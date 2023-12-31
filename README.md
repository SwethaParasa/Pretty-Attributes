# Pretty-Attributes
Pretty Parser for BMC Device Tree

-------------------------------------------------------------------------------------------------------------------------
Pretty Attribute Parser
Usage
         pretty-attributes [option [<target>/<path>] [-j] [<-limited>/<attribute1,attribute2,...>]]
                  -If no option is provided, information about all targets will be displayed.
         pretty-attributes export [<attr-list>]
         pretty-attributes import <attr-dump>
         pretty-attributes read <target>/<path> <attribute>
         pretty-attributes write <target>/<path> <attribute> <value>
         pretty-attributes translate <target>/<path>

Options
       -t,-target    
              --> Specify a target to display information about that specific target.
                  usage : pretty-attributes -t[arget] <cronus_name_of_the_target> [-j] [<-limited>/<attribute1,attribute2,...>]
       
       -p,-path
              --> Provide a physical path to display information about the target located at that path.
	          usage : pretty-attributes -p[ath] <physical_path> [-j] [<-limited>/<attribute1,attribute2,...>]
	
       -n,-nodes
              --> Print the hierarchical structure of nodes.
              --> If a path is specified, the subtree rooted at that path will be displayed.
	          usage : pretty-attributes -n[odes] [-fullpath <full_physical_path>]  [<physical_path>]

       -l,-list
              --> Lists all available targets.
		  usage : pretty-attributes -l[ist]
       -j,-json
              --> Print target information in JSON format.
       -limited
              --> Print Limited information about all targets.
       -f,-find
	      --> Displays a list of attributes for the specified target. (For example, We can get list of cores, dimms etc.)
		  usage : pretty-attributes -f[ind] <target> [attribute1=value attribute2=value ...]
       -parent
             --> Displays the parent of given target
                usage : pretty-attributes -parent <cronus_of_target>
       -child
             --> Displays the children of given target
                usage : pretty-attributes -child <cronus_of_target>
       -host
             --> Specify BMC to get connected (give -host <hostname> at the end if the command)(By default it is rain100bmc.aus.stglabs.ibm.com)
                usage : pretty-attributes [specify-options] -host <hostname> 
       -password
             --> Specify Password to get connected (give -password <password> at the end if the command)(By default it is 0penBmc0)
                usage : pretty-attributes [specify-options] -password <password>
       -user
             --> Specify username to get connected (give -user <username> at the end if the command)(By default it is service)
                usage : pretty-attributes [specify-options] -user <username>

       export
              --> Used to print all attribute values.
       import
              --> Used to update device tree with attribute values.
       read
              --> Used to print a single attribute value for a target.
       write
              --> Used to modify a single attribute value for a target.
       translate
             --> Used to translate target name between cronus and device tree.
       <attr-list>
             --> Filename containing list of attribute names to export.
       <attr-dump>
             --> Filename containing targets and attribute values.
       <target>
             --> Device tree target, e.g. p10:k0:n0:s0:p00 (cronus).
       <path>
             --> Device tree path, e.g. /sys-0/node-0/proc0 (device tree path).
       <value>
             --> Value of the attribute.
       <attribute>
             --> Name of an attribute.
-------------------------------------------------------------------------------------------------------------------------
