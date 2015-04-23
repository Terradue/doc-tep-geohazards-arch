Engineering Viewpoint - Deployment nodes
########################################

.. uml::

	skinparam component {
	    BackgroundColor<<tep>> RosyBrown
	    BorderColor<<tep>> black
	}

	cloud "Terradue Private Cloud" {

		node "Proxy" {
			[HTTP Proxy Server] -- [Web Service Firewall]
		}

		node "VPN Gateway" {
			[OpenVPN Server] .. [Cloud Firewall] : dynamic rules
			[OpenVPN Server] -- [Cloud Firewall]
		}

		node "Cloud Controller" {
		  [HTTP Sunstone Dashboard] -- [OpenNebula] : XML-RPC
		} 

		

		frame "Virtual Hosts" {

			package "Terradue Service" {

				node "Web Portal" << VM >> {
				  [HTTP Web Portal Server] << tep >> 
				  database "MySql" {
				  	[DB Tep]
				  }
				  [HTTP Web Portal Server] -- [DB Tep]
				} 

				node "Catalogue" << VM >> {
				  [HTTP OpenSearch Catalogue] << tep >> 
				  database "ElasticSearch" {
				  	[Index EO]
				  }
				  [HTTP OpenSearch Catalogue] -- [Index EO]
				}

			}

			package "Users" {
				node "Developer Cloud Sandbox" << VM >> {
				  	[HTTP Sandbox Dashboard] -- [User App]
				  	[Sandbox WPS Server] -- [User App]
				  	[SSH Server] -- [User App]
				}

				node "ESA CloudToolbox" << VM >> {
					[VNC Server] -- [Sentinel-1 toolbox]
					[VNC Server] -- [NEST]
					[VNC Server] -- [GAMMA]
					[VNC Server] -- [Matlab]

				}
			}
			
		}

		[HTTP Web Portal Server] -- [Sandbox WPS Server] : HTTP
		[HTTP Web Portal Server] -- [OpenNebula] : XML-RPC

		[Web Service Firewall] -- [HTTP Web Portal Server] : HTTP
		[Web Service Firewall] -- [HTTP OpenSearch Catalogue] : HTTP
		[Web Service Firewall] -- [HTTP Sunstone Dashboard] : HTTP

		[Cloud Firewall] -- [VNC Server]
		[Cloud Firewall] -- [SSH Server] : SSH
		[Cloud Firewall] -- [HTTP Sandbox Dashboard] : HTTP
	}

	() "https://geohazards-tep.eo.esa.int/" -- [HTTP Proxy Server] : HTTPS
	() "https://access.terradue.com/" -- [OpenVPN Server] : HTTPS
	() "https://cloud.terradue.com/" -- [HTTP Proxy Server] : HTTPS

