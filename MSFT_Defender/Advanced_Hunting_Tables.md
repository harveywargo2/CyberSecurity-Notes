# References
- https://learn.microsoft.com/en-us/defender-xdr/advanced-hunting-schema-tables?view=o365-worldwide
- https://learn.microsoft.com/en-us/microsoft-365/security/defender/advanced-hunting-schema-tables?view=o365-worldwide

# Action types 
- possible values in the `ActionType` column representing the event types supported by the table. 
- This information is provided only for tables that contain event information 

##### DeviceProcessEvents - Sysmon EID 1
- Process Create

#### DeviceFileEvents - Sysmon EID 11 & EID 23
- FileCreated
- FileRenamed
- FileModified
- FileDeleted

#### DeviceNetworkEvents - Sysmon EID 3
- ConnectionSuccess
- NetworkSignatureInspected
- ListeningConnectionCreated
- ConnectionFailed
- ConnectionRequest
- InboundConnectionAccepted
- ConnectionFound

#### DeviceLogonEvents - WinSecLog EID 4624
- LogonAttempted
- LogonSuccess
- LogonFailed

#### DeviceRegistryEvents - Sysmon EID 12 & EID 13
- RegistryValueSet
- RegistryValueDeleted
- RegistryKeyDeleted
- RegistryKeyCreated
- RegistryKeyRenamed

#### DeviceImageLoadEvents - Sysmon EID 7 

#### DeviceEvents
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