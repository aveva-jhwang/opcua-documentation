---
uid: ReleaseNotesOPCUA
---

# AVEVA Adapter for OPC UA

AVEVA Adapter for OPC UA: 1.4.0.196<br>

Adapter Framework: 1.7

## Overview

AVEVA Adapter for OPC UA collects time series data and relevant metadata from an OPC UA (OPC Unified Architecture) server and sends it to configured "Open MessageFormat (OMF) endpoints such as PI Web API and AVEVA Data Hub. AVEVA Adapter for OPC UA can also collect health and diagnostics information. It supports buffering, unsolicited data collection, on-demand discovery of available data items on a data source, on-demand or automatic history recovery of data items, and various Windows and Linux-based operating systems as well as containerization.

This version is released with the support for client failover and server failover functionality.

For more information see [AVEVA Adapter for OPC UA overview](xref:AVEVAAdapterForOPCUAOverview).

## Fixes and enhancements

### Fixes

The following issues reported from earlier versions are fixed in this release.

- Data collection for the OPC UA server data items will no longer be skipped when the source OPC UA Server has invalid data item attributes like: DataType, Description, BrowseName, DisplayName, UserAccessLevel.
- History recovery starttime and endtime supplied in local time format will be treated as a local time by the adapter node instead of the UTC time.
- The OpcUa Data Type 'UtcTime' is now supported as a DateTime type.

### Enhancements

The following enhancements are added in this release.

- Reduce load on OPC UA server during history recovery by caching user access level.
- Enhanced logged messages to include status code in hexadecimal instead of decimal and aliased data types.
- Manage edge system configuration secrets in a centralized location while keeping backward compatibility.
- Exclude read-only facets from top level configuration in Get request.
- Increase the payload size to 64MB.
- No longer log and throw System.InvalidOperationException when the same component is added multiple times.
- The DeviceStatus value "NotConfigured" has been changed to "Not Configured."
- Server failover support for AVEVA Adapter for OPC UA.
- Client failover support for AVEVA Adapter for OPC UA.

## Known issues

There are no known issues at this time.

## Setup

### System requirements

Refer to [System requirements](xref:SystemRequirements).

### Installation and upgrade

Refer to [Install the adapter](xref:InstallTheAdapter).

### Uninstallation

Refer to [Uninstall the adapter](xref:UninstallTheAdapter).

## Security information and guidance

OSIsoft is [committed to releasing secure products](https://docs.osisoft.com/bundle/security-commitment-and-disclosure-standards/page/securitycommitmentanddisclosurestandards.html). This section is intended to provide relevant security-related information to guide your installation or upgrade decision.  

OSIsoft [proactively discloses](https://docs.osisoft.com/bundle/security-commitment-and-disclosure-standards/page/securitycommitmentanddisclosurestandards.html#vulnerability-communication) aggregate information about the number and severity of security vulnerabilities addressed in each release. The tables below provide an overview of security issues addressed and their relative severity based on [standard scoring](https://docs.osisoft.com/bundle/security-commitment-and-disclosure-standards/page/securitycommitmentanddisclosurestandards.html#vulnerability-scoring). 

### Overview of new vulnerabilities found or fixed

This section is intended to provide relevant security-related information to guide your installation or upgrade decision. OSIsoft is proactively disclosing aggregate information about the number and severity of AVEVA Adapter for OPC UA security vulnerabilities that are fixed in this release.

| Component | Version | CVE or Reference | CVSS | Mitigation                                                                                                 |
| ----------| ------- | --------------------------------------------------------------------------------------------------- | ---- | ---------------------------------------------------------------------------------------------------------- |
| zlib      | 1.2.11  | [CVE-2018-25032](https://nvd.nist.gov/vuln/detail/CVE-2018-25032)                                   | 7.5  | The AVEVA Adapter’s utilization of zlib through the .NET 6 Framework does not expose these vulnerabilities  |                                                      |
| zlib      | 1.2.11  | [BSDA-2018-5271](https://osisoft.blackducksoftware.com/api/vulnerabilities/BDSA-2018-5271/overview) | 7.1  | The AVEVA Adapter’s utilization of zlib through the .NET 6 Framework does not expose these vulnerabilities. |
| zlib      | 1.2.11  | [CVE-2022-37434](https://nvd.nist.gov/vuln/detail/CVE-2022-37434)                                   | 9.3  | The AVEVA Adapter’s utilization of zlib through the .NET 6 Framework does not expose these vulnerabilities. |

## Documentation overview

[EdgeCmd utility](https://docs.osisoft.com/bundle/edgecmd/page/index.html): Provides an overview on how to configure and administer AVEVA Adapters on Linux and Windows using command line arguments.

## Technical support and resources

Refer to [Technical support and feedback](xref:TechnicalSupportAndFeedback).
