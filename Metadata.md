Metadata represents data about data. Metadata enriches the data with information that makes it easier to find, use and manage. For example, [[HTML]] tags define layout for human readers. Semantic metadata helps computers to interpret data by adding references to concepts in a knowledge graph.

-   Data that provide information about other data.
-   Metadata return information about the instance that's recorded localy.
-   Metadata can be created manually to be more accurate, or automatically and contain more basic information.
-   Metadata summarizes basic information about data and making finding & working with particular instances of data easier.

## Instance Metadata

Instance metadata is data about your [[EC2]] instance that you can use to configure or manage the running instance.

-   Instance metadata is data about your EC2 instance
-   [[User data]] and metadata are not encrypted
-   Instance metadata is available at: ==http://169.254.169.254/latest/meta-data/
-   The Instance Metadata Query tool allows you to query the instance metadata without having to type out the full [[URI]] or category names.


## Query metadata 
#command

List metadata information you can return:

	curl http://169.254.169.254/latest/meta-data/

![[Pasted image 20230201101528.png]]

You can query this information if you add the name in the end of the link

	curl http://169.254.169.254/latest/meta-data/local-ipv4

![[Pasted image 20230201101651.png]]

