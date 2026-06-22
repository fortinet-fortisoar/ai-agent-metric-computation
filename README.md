# Release Information

- **Version**: 1.0.0

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: Core and Orchestration, Insights

- **Verified with Models**: Fortinet FortiAI (AI model Large)

# Metric Computation Agent

Computes metrics from structured data based on natural-language instructions. Supports aggregations, counting, statistical calculations, timestamp and duration analysis, trend analysis, and lightweight correlation. All calculations are derived directly from the provided dataset, with no estimation or inference of missing values.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

**Required MCP Servers**: NA

<!-- > [!Note]
>
> Refer to [Configuring MCP Servers](https://docs.fortinet.com/document/fortisoar/8.0.0/administration-guide/823139/mcp-servers#Configure_MCP_Servers) on FortiSOAR platform documentation for information on configuring a custom MCP server.
>  -->

### Prerequisites

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
>
> FortiAI solution pack and Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.0`.
> 


## Input Parameters

The input must be provided as a JSON object.

| Parameter               | Description                                                                                                               |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `natural_language_task` | Instruction describing what metrics should be generated or calculated from the provided data.                             |
| `data`                  | Structured dataset containing records, events, timestamps, or numerical values used as the source for metric computation. |


## Response

The output is returned as a JSON object.

| Parameter | Description                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `status`  | Indicates whether the metric calculation completed successfully or failed.                                             |
| `data`    | Structured output containing calculated metrics, the final result, and an explanation of how the metrics were derived. |

