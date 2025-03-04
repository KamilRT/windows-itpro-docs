---
title: Policy CSP - ADMX_DiskDiagnostic
description: Policy CSP - ADMX_DiskDiagnostic
ms.author: dansimp
ms.localizationpriority: medium
ms.topic: article
ms.prod: w10
ms.technology: windows
author: nimishasatapathy
ms.date: 09/08/2021
ms.reviewer: 
manager: dansimp
---

# Policy CSP - ADMX_DiskDiagnostic
> [!WARNING]
> Some information relates to prereleased products, which may be substantially modified before it's commercially released. Microsoft makes no warranties, expressed or implied, concerning the information provided here.

<hr/>

<!--Policies-->
## ADMX_DiskDiagnostic policies  

<dl>
  <dd>
    <a href="#admx-diskdiagnostic-dfdalertpolicy">ADMX_DiskDiagnostic/DfdAlertPolicy</a>
  </dd>
  <dd>
    <a href="#admx-diskdiagnostic-wdiscenarioexecutionpolicy">ADMX_DiskDiagnostic/WdiScenarioExecutionPolicy</a>
  </dd>
</dl>


<hr/>

<!--Policy-->
<a href="" id="admx-diskdiagnostic-dfdalertpolicy"></a>**ADMX_DiskDiagnostic/DfdAlertPolicy**  

<!--SupportedSKUs-->
<table>
<tr>
    <th>Edition</th>
    <th>Windows 10</th>
    <th>Windows 11</th>
</tr>
<tr>
    <td>Home</td>
    <td>No</td>
    <td>No</td>
</tr>
<tr>
    <td>Pro</td>
    <td>No</td>
    <td>No</td>
<tr>
    <td>Business</td>
    <td>No</td>
    <td>No</td>
</tr>
<tr>
    <td>Enterprise</td>
    <td>Yes</td>
    <td>Yes</td>
</tr>
<tr>
    <td>Education</td>
    <td>Yes</td>
    <td>Yes</td>
</tr>
</table>

<!--/SupportedSKUs-->
<hr/>

<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
This policy setting substitutes custom alert text in the disk diagnostic message shown to users when a disk reports a S.M.A.R.T. fault.

- If you enable this policy setting, Windows displays custom alert text in the disk diagnostic message. The custom text may not exceed 512 characters.
- If you disable or do not configure this policy setting, Windows displays the default alert text in the disk diagnostic message. 

No reboots or service restarts are required for this policy setting to take effect: changes take effect immediately. 

This policy setting only takes effect if the Disk Diagnostic scenario policy setting is enabled or not configured and the Diagnostic Policy Service (DPS) is in the running state. When the service is stopped or disabled, diagnostic scenarios are not executed. 
The DPS can be configured with the Services snap-in to the Microsoft Management Console.

> [!NOTE]
> For Windows Server systems, this policy setting applies only if the Desktop Experience optional component is installed and the Remote Desktop Services.

<!--/Description-->
> [!TIP]
> This is an ADMX-backed policy and requires a special SyncML format to enable or disable. For details, see [Understanding ADMX-backed policies](./understanding-admx-backed-policies.md).
> 
> You must specify the data type in the SyncML as &lt;Format&gt;chr&lt;/Format&gt;. For an example SyncML, refer to [Enabling a policy](./understanding-admx-backed-policies.md#enabling-a-policy).
> 
> The payload of the SyncML must be XML-encoded; for this XML encoding, there are a variety of online encoders that you can use. To avoid encoding the payload, you can use CDATA if your MDM supports it. For more information, see [CDATA Sections](http://www.w3.org/TR/REC-xml/#sec-cdata-sect).

<!--ADMXBacked-->
ADMX Info:  
-   GP Friendly name: *Configure custom alert text*
-   GP name: *DfdAlertPolicy*
-   GP path: *System\Troubleshooting and Diagnostics\Disk Diagnostic*
-   GP ADMX file name: *DiskDiagnostic.admx*

<!--/ADMXBacked-->
<!--/Policy-->
<hr/>
<hr/>

<!--Policy-->
<a href="" id="admx-diskdiagnostic-wdiscenarioexecutionpolicy"></a>**ADMX_DiskDiagnostic/WdiScenarioExecutionPolicy**  

<!--SupportedSKUs-->
<table>
<tr>
    <th>Edition</th>
    <th>Windows 10</th>
    <th>Windows 11</th>
</tr>
<tr>
    <td>Home</td>
    <td>No</td>
    <td>No</td>
</tr>
<tr>
    <td>Pro</td>
    <td>No</td>
    <td>No</td>
<tr>
    <td>Business</td>
    <td>No</td>
    <td>No</td>
</tr>
<tr>
    <td>Enterprise</td>
    <td>Yes</td>
    <td>Yes</td>
</tr>
<tr>
    <td>Education</td>
    <td>Yes</td>
    <td>Yes</td>
</tr>
</table>

<!--/SupportedSKUs-->
<hr/>

<!--Scope-->
[Scope](./policy-configuration-service-provider.md#policy-scope):

> [!div class = "checklist"]
> * Device

<hr/>

<!--/Scope-->
<!--Description-->
This policy setting determines the execution level for S.M.A.R.T.-based disk diagnostics. 

Self-Monitoring And Reporting Technology (S.M.A.R.T.) is a standard mechanism for storage devices to report faults to Windows. A disk that reports a S.M.A.R.T. fault may need to be repaired or replaced. The Diagnostic Policy Service (DPS) detects and logs S.M.A.R.T. faults to the event log when they occur.
  
- If you enable this policy setting, the DPS also warns users of S.M.A.R.T. faults and guides them through backup and recovery to minimize potential data loss.  
- If you disable this policy, S.M.A.R.T. faults are still detected and logged, but no corrective action is taken. 
- If you do not configure this policy setting, the DPS enables S.M.A.R.T. fault resolution by default. This policy setting takes effect only if the diagnostics-wide scenario execution policy is not configured.  

No reboots or service restarts are required for this policy setting to take effect: changes take effect immediately. 
This policy setting takes effect only when the DPS is in the running state. When the service is stopped or disabled, diagnostic scenarios are not executed. The DPS can be configured with the Services snap-in to the Microsoft Management Console. 

> [!NOTE]
> For Windows Server systems, this policy setting applies only if the Desktop Experience optional component is installed and the Remote Desktop Services role is not installed.
			
<!--/Description-->
> [!TIP]
> This is an ADMX-backed policy and requires a special SyncML format to enable or disable. For details, see [Understanding ADMX-backed policies](./understanding-admx-backed-policies.md).
> 
> You must specify the data type in the SyncML as &lt;Format&gt;chr&lt;/Format&gt;. For an example SyncML, refer to [Enabling a policy](./understanding-admx-backed-policies.md#enabling-a-policy).
> 
> The payload of the SyncML must be XML-encoded; for this XML encoding, there are a variety of online encoders that you can use. To avoid encoding the payload, you can use CDATA if your MDM supports it. For more information, see [CDATA Sections](http://www.w3.org/TR/REC-xml/#sec-cdata-sect).

<!--ADMXBacked-->
ADMX Info:  
-   GP Friendly name: *Configure execution level*
-   GP name: *WdiScenarioExecutionPolicy*
-   GP path: *System\Troubleshooting and Diagnostics\Disk Diagnostic*
-   GP ADMX file name: *DiskDiagnostic.admx*

<!--/ADMXBacked-->
<!--/Policy-->
<hr/>

> [!NOTE]
> These policies are for upcoming release.

<!--/Policies-->

