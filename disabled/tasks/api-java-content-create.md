---
author: [Alfresco Documentation, Alfresco Documentation]
source: Professional Alfresco Book
audience: 
category: [Java Foundation, Services, API/Script]
keyword: [Java API, Java Foundation]
---

# Using the Java API to create new content

This example uses the Java API `NodeService` and `ContentService` Embedded API to create new content.

This example takes a `nodeRef` of the folder containing the node, a string to be used for the nodes name, and a string containing the content. A map of metadata data values is created and passed as a parameter to the NodeServer that creates the node. The content is written to the node using the `ContentService` and returns the node reference for the new node.

-   Create new content using the Java API with the following code sample \(`createContentNode.java`\).

    ```
    /**
     * Creates a new content node setting the content provided.
     *
     * @param  parent   the parent node reference
     * @param  name     the name of the newly created content object
     * @param  text     the content text to be set on the newly created node
     * @return NodeRef  node reference to the newly created content node
     *
    private NodeRef createContentNode(NodeRef parent, String name, String text)
        {
    
     // Create a map to contain the values of the properties of the node
            
            Map<QName, Serializable> props = new HashMap<QName, Serializable>(1);
            props.put(ContentModel.PROP_NAME, name);  
    
    // use the node service to create a new node
            NodeRef node = this.nodeService.createNode(
                            parent, 
                            ContentModel.ASSOC_CONTAINS, 
                            QName.createQName(NamespaceService.CONTENT_MODEL_1_0_URI, name),
                            ContentModel.TYPE_CONTENT, 
                            props).getChildRef();   
    ```


**Parent topic:**[Using Embedded APIs](../concepts/serv-api-embedded-about.md)

**Related information**  


[Using Embedded APIs](../concepts/serv-api-embedded-about.md)

