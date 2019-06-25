# Scheduling Configuration {#concept_185601 .concept}

Logical tables support viewing and configuring scheduling information.

[Go to the logical table editing page](intl.en-US/User Guide/Data modeling and development/Logical tables: Logical dimension tables/Configure logical models and tables.md#section_ysx_sb3_fhb), and select **Scheduling Configuration** tab on the page. You can view and configure the basic information, scheduling recurrence, and scheduling dependencies of the logical table. The configuration is directly applied to the scheduling of logical tables, automatic coding, and code execution.

The instructions are described as follows:

-   Basic Information: Enter the required information. You can enter custom parameters in the text box following **Parameter Configuration**. Multiple parameters are separated by semicolons \(;\).
-   Recurrence: You can select Yes or No for Depend On Previous Instance. If you select **Yes**, the logical table task is scheduled to run after the previous task instance is complete.
-   Dependency: In this section, you can configure and manage automatic parsing, upstream dependencies, and the output of a logical table.

    -   Automatic Parse: The system can automatically parse the upstream dependency and output of a logical table. Based on whether the upstream node is generated by logical table conversion, the content of upstream dependency parsing is categorized into two types: **logical table conversion dependency** and **regular dependency**. Click **Parse Input and Output** again, the upstream dependency and the output of the logical table are refreshed.
    -   Upstream dependency: Displays the parent nodes that are depended by this node.

        Click **Parse Error Information**. In the information box that appears, the source physical table in the source code and the impacted field that is not parsed for the corresponding associated node ID are displayed. If there are multiple source physical tables and impacted fields, they will be displayed in a vertical mode as pairs. To add these tables and fields to the upstream dependency, click **Add Upstream Dependency** under the source physical tables and impacted fields, as shown in the following figure.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/150110/156134674041737_en-US.png)

    -   Logical table output: Displays all output nodes of the logical table. The information displayed includes the current node output name, node name, node ID, and owner. You can click the expand icon to display all **level-1 downstream node** information for the current node, including the downstream node name and downstream node ID.
    **Note:** The output of a logical table is automatically generated by the system. Upstream nodes of a logical table are referenced tables that are parsed in the logical table code. You can add the node whose output name is same as the table name as a depended upstream node. The ID of a code task node or a sync task node in the production environment is the same as that in the development environment. The ID of a logical table task node in the production environment is different from that in the development environment. You can go to the **scheduling center** to learn more about the logical table nodes and instances. For more information about the scheduling center, see [Overview](intl.en-US/User Guide/Scheduling center/Overview.md#).

