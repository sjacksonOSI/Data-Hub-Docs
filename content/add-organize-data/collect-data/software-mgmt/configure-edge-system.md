---
uid: ManageConfigurations
---

# Manage system configurations

You can import a system configuration from the field to its corresponding system digital twin as a record. You can also create a new configuration, using a default configuration or a configuration template. Once the configuration is complete, you can export the configuration file for each component or for the system. You can use an exported configuration file to configure other systems by importing it. The maximum size for a configuration file is 16 MB.

Configuration is available for the following system types:

 - AVEVA Adapter for Azure Event Hubs

 - AVEVA Adapter for BACnet

 - AVEVA Adapter for DNP3

 - Edge Data Store

 - AVEVA Adapter for Modbus TCP

 - AVEVA Adapter for MQTT

 - AVEVA Adapter for OPC UA

 - AVEVA Adapter for RDBMS

 - AVEVA Adapter for Structured Data Files

The `namespaceId` in the data and health endpoint URLs defaults to the namespace where the configuration template is created. For example, if the namespace of the configuration template is MyData, the endpoint URL would be `https://website.com/api/v1/Tenants/{tenantId}/Namespaces/MyData/Omf`.

A system appears on the `Edge Data Store & Adapters Systems` page once it is writing health data to AVEVA Data Hub. For information on configuring health endpoints, see the specific system product documentation at [docs.aveva.com](https://docs.aveva.com/).

For systems, use mustache tokens, in the format `{{SecretA}}`, to denote secrets in configuration files. Secrets are managed using clients. The token name must match an Edge Management System property defined for the system. Tokens must be used in fields where `isEncrypted=true`. After deploying the configuration to the device, you must manually update the configuration on the device with the secret.

For edge modules, use variables, in the format `{{VariableA}}`, to denote secrets in configuration files. The variable is associated with a secret in AVEVA Edge Management.

## Import a system configuration

To import a system configuration from the field to the corresponding system digital twin:

1. In the left pane, select **Data Collection** > **Edge Data Store & Adapters**.

1. Verify that the **Systems/Configuration Templates** selector is set to **Systems**.

1. Find and select the edge device to configure.

1. Select **Edit System**.

1. Select **Import Configuration**.

1. In the `Import Configuration` window, click **Select file**, browse to the configuration file to import, and then select **Open**.

1. Select **Import**.

1. Review the imported file contents to ensure it is correct.

1. When you have finished, select **Save & Close**.

1. To confirm the changes, select **Save & Close**.

## Edit an system configuration

To edit a system configuration and export it for use:

1. In the left pane, select **Data Collection** > **Edge Data Store & Adapters**.

1. Verify that the **Systems/Configuration Templates** selector is set to **Systems**.

1. Find and select the edge device to configure.

1. In the right pane, select **Edit System** or ![Edit](../../../_icons/default/pencil.svg).

1. To manage the tags for a system, select **Add Tag** ![Add Tag](../../../_icons/default/plus.svg) and then do the following:

   - To add a tag, enter the tag text in the **New Tag** field and press Enter.

   - To delete a tag, select **X** in the tag bubble.

1. To create the configuration, do one of the following:

   - To use the default configuration for the system type, select **Start With Default**.

   - To select a JSON file that contains the configuration, select **Start With Default**.

1. (Optional) In the **Section Select** dropdown list, select the section of the configuration to modify. The default option of `JSON Configuration` shows the entire configuration.

1. Modify the JSON as needed. For configuration guidelines, refer to the specific system documentation.

   **WARNING:** Do not include secrets in the configuration. Secrets cannot be stored or exported in a configuration. 

   Errors in the JSON syntax are underlined. To see an explanation of the issue, hold the mouse over the underlined text. The overall status of the JSON syntax is displayed over the right pane.

1. To export the completed configuration, do one of the following:

   - To export just the selected section, select **Export Section** in the right pane.

   - To export the entire configuration in one file, select **Export Configuration**.

   The JSON file is downloaded to your browser.

1. When you have finished, select **Save & Close**.

1. To confirm the changes, select **Save & Close**.
