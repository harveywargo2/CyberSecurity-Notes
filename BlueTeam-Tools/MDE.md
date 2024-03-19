
## MDE Response & Remediate References
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/respond-machine-alerts?view=o365-worldwide

## MDE Analysis & DFIR References
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/advanced-hunting-overview?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/device-timeline-event-flag?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/investigate-files?view=o365-worldwide#observed-in-organization
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/device-timeline-event-flag?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/investigate-alerts?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/machines-view-overview?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/investigate-user?view=o365-
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/?view=o365-worldwide 
- https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/overview-endpoint-detection-response?view=o365-worldwide


## MDE Detection & Hunting References
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/custom-detections-overview?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/custom-detection-rules?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/advanced-hunting-overview?view=o365-worldwide


## AMSI Anti Malware Scan Interface
- https://docs.microsoft.com/en-us/windows/win32/amsi/how-amsi-helps
- https://learn.microsoft.com/en-us/windows/win32/amsi/antimalware-scan-interface-portal


## Attack Surface Reduction Rules
- https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/attack-surface-reduction-rules-reference?view=o365-worldwide#block-all-office-applications-from-creating-child-processes


## API 
- https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/run-advanced-query-api?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/api-overview?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/api-supported?view=o365-worldwide

## Data Schema
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/advanced-hunting-deviceprocessevents-table?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/advanced-hunting-schema-tables?view=o365-worldwide

**Action types**—possible values in the `ActionType` column representing the event types supported by the table. This information is provided only for tables that contain event information 

#### Notable Action Types Per Table
DeviceProcessEvents - Sysmon EID 1
- Process Create

DeviceFileEvents - Sysmon EID 11 & EID 23
- FileCreated
- FileRenamed
- FileModified
- FileDeleted

DeviceNetworkEvents - Sysmon EID 3
- ConnectionSuccess
- NetworkSignatureInspected
- ListeningConnectionCreated
- ConnectionFailed
- ConnectionRequest
- InboundConnectionAccepted
- ConnectionFound

DeviceLogonEvents - WinSecLog EID 4624
- LogonAttempted
- LogonSuccess
- LogonFailed

DeviceRegistryEvents - Sysmon EID 12 & EID 13
- RegistryValueSet
- RegistryValueDeleted
- RegistryKeyDeleted
- RegistryKeyCreated
- RegistryKeyRenamed

DeviceImageLoadEvents - Sysmon EID 7 

DeviceEvents
>   
AmsiScriptDetection  
AntivirusDetection  
AntivirusDetectionActionType  
AntivirusReport  
AntivirusScanCancelled  
AntivirusScanCompleted  
AntivirusScanFailed  
AppControlAppInstallationBlocked  
AppControlCIScriptAudited  
AppControlCIScriptBlocked  
AppControlCodeIntegrityDriverRevoked  
AppControlCodeIntegrityOriginAudited  
AppControlCodeIntegrityPolicyAudited  
AppControlCodeIntegrityPolicyBlocked  
AppControlCodeIntegrityPolicyLoaded  
AppControlCodeIntegritySigningInformation  
AppControlExecutableAudited  
AppControlExecutableBlocked  
AppControlPackagedAppBlocked  
AppControlPolicyApplied  
AppControlScriptAudited  
AppGuardBrowseToUrl  
AppGuardCreateContainer  
AppGuardStopContainer  
AppGuardSuspendContainer  
AsrAdobeReaderChildProcessAudited  
AsrCustomRuleAudited  
AsrExecutableEmailContentAudited  
AsrExecutableEmailContentBlocked  
AsrExecutableOfficeContentAudited  
AsrExecutableOfficeContentBlocked  
AsrLsassCredentialTheftAudited  
AsrLsassCredentialTheftBlocked  
AsrObfuscatedScriptAudited  
AsrOfficeChildProcessAudited  
AsrOfficeCommAppChildProcessAudited  
AsrOfficeMacroWin32ApiCallsAudited  
AsrOfficeProcessInjectionAudited  
AsrPersistenceThroughWmiAudited  
AsrPsexecWmiChildProcessAudited  
AsrPsexecWmiChildProcessBlocked  
AsrRansomwareAudited  
AsrScriptExecutableDownloadAudited  
AsrUntrustedExecutableAudited  
AsrUntrustedUsbProcessAudited  
AsrUntrustedUsbProcessBlocked  
AuditPolicyModification  
BluetoothPolicyTriggered  
BrowserLaunchedToOpenUrl  
ClrUnbackedModuleLoaded  
ContainedUserLogonBlocked  
ContainedUserRemoteDesktopSessionDisconnected  
ContainedUserRemoteDesktopSessionStopped  
ContainedUserSmbFileOpenBlocked  
ControlFlowGuardViolation  
ControlledFolderAccessViolationAudited  
ControlledFolderAccessViolationBlocked  
CreateRemoteThreadApiCall  
DirectoryServiceObjectCreated  
DnsQueryResponse  
DpapiAccessed  
DriverLoad  
ExploitGuardAcgAudited  
ExploitGuardAcgEnforced  
ExploitGuardChildProcessAudited  
ExploitGuardChildProcessBlocked  
ExploitGuardLowIntegrityImageAudited  
ExploitGuardLowIntegrityImageBlocked  
ExploitGuardNetworkProtectionAudited  
ExploitGuardNonMicrosoftSignedAudited  
ExploitGuardNonMicrosoftSignedBlocked  
ExploitGuardSharedBinaryAudited  
ExploitGuardSharedBinaryBlocked  
ExploitGuardWin32SystemCallAudited  
ExploitGuardWin32SystemCallBlocked  
FirewallInboundConnectionBlocked  
FirewallInboundConnectionToAppBlocked  
FirewallOutboundConnectionBlocked  
FirewallServiceStopped  
GetAsyncKeyStateApiCall  
GetClipboardData  
LdapSearch  
MemoryRemoteProtect  
NamedPipeEvent  
NtAllocateVirtualMemoryApiCall  
NtAllocateVirtualMemoryRemoteApiCall  
NtMapViewOfSectionRemoteApiCall  
NtProtectVirtualMemoryApiCall  
OpenProcessApiCall  
OtherAlertRelatedActivity  
PlistPropertyModified  
PnpDeviceAllowed  
PnpDeviceConnected  
PowerShellCommand  
ProcessCreatedUsingWmiQuery  
ProcessPrimaryTokenModified  
QueueUserApcRemoteApiCall  
ReadProcessMemoryApiCall  
RemoteDesktopConnection  
RemoteWmiOperation  
SafeDocFileScan  
ScheduledTaskCreated  
ScheduledTaskDeleted  
ScheduledTaskUpdated  
ScreenshotTaken  
ScriptContent  
SecurityGroupCreated  
SecurityGroupDeleted  
SecurityLogCleared  
SensitiveFileRead  
ServiceInstalled  
SetThreadContextRemoteApiCall  
ShellLinkCreateFileEvent  
SmartScreenAppWarning  
SmartScreenUrlWarning  
SmartScreenUserOverride  
TamperingAttempt  
TvmAxonTelemetryEvent  
UntrustedWifiConnection  
UsbDriveDriveLetterChanged  
UsbDriveMounted  
UsbDriveUnmounted  
UserAccountAddedToLocalGroup  
UserAccountCreated  
UserAccountDeleted  
UserAccountModified  
UserAccountRemovedFromLocalGroup  
WmiBindEventFilterToConsumer  
WriteToLsassProcessMemory
