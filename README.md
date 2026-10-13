# BIP_launch_service_provider

## Project Overview

SmartConnect France is a prototype of an SD-WAN-enabled Internet Service Provider (ISP) designed for French households. The project aims to improve internet reliability by combining a primary internet connection with a backup connection and automatically switching to the backup when the primary connection fails.

The prototype is developed in a virtual lab and includes a network monitoring dashboard to visualize connectivity status and failover events.

## Objectives

- Simulate a household network with two WAN connections.
- Configure automatic primary-to-backup failover.
- Monitor WAN availability and network performance.
- Develop a dashboard for network status and measurements.
- Evaluate the reliability and performance of the solution through repeatable tests.

## Technologies

- **GNS3** — Virtual network simulation.
- **OpenWrt** — Virtual household router.
- **mwan3** — Multi-WAN monitoring and failover.
- **Python** — Monitoring and data processing.
- **Streamlit** — Interactive dashboard.
- **Plotly and Pandas** — Data visualization and analysis.
- **Git** — Version control and team collaboration.

## Architecture

The virtual topology consists of:

- A household client connected to an OpenWrt router.
- A simulated primary WAN connection representing fiber.
- A simulated backup WAN connection representing 4G/5G.
- A monitoring dashboard displaying network status and measurements.

When the primary connection fails, OpenWrt uses the configured failover policy to route new outbound connections through the backup connection.

## Team Organization

The project is developed by a team of four:

1. **Network Simulation:** GNS3 topology and IP configuration.
2. **Router Configuration:** OpenWrt, mwan3 and automatic failover.
3. **Dashboard Development:** Python, Streamlit and monitoring.
4. **Integration and Testing:** Validation, documentation and business analysis.

## Testing and Evaluation

The prototype will be evaluated by:

- Verifying connectivity through both WAN paths.
- Simulating primary connection failures.
- Measuring failover detection and recovery times.
- Testing recovery when the primary connection returns.
- Monitoring network status and recording test results.

Target criteria include detecting primary-link failure within 15 seconds and restoring new outbound connectivity through the backup within 20 seconds in at least 9 out of 10 trials. Actual results will be documented after testing.

## Project Scope

This project is an educational, SD-WAN-style multi-WAN failover prototype. Both internet connections are simulated; the project does not provide real internet service or represent measured French ISP performance.

## Expected Deliverables

- Working GNS3 virtual network.
- OpenWrt router with automatic WAN failover.
- Interactive network monitoring dashboard.
- Test results and performance measurements.
- Technical documentation and final presentation.
