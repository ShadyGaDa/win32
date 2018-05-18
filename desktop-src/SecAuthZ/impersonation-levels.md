---
Description: 'The SECURITY\_IMPERSONATION\_LEVEL enumeration defines four impersonation levels that determine the operations a server can perform in the client's context.'
ms.assetid: 'ae152dbf-44f0-417f-a85e-09bf60dcfcb0'
title: Impersonation Levels
---

# Impersonation Levels

The [**SECURITY\_IMPERSONATION\_LEVEL**](security-impersonation-level.md) enumeration defines four impersonation levels that determine the operations a server can perform in the client's context.



| Impersonation level    | Description                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | The server cannot impersonate or identify the client.                                            |
| SecurityIdentification | The server can get the identity and privileges of the client, but cannot impersonate the client. |
| SecurityImpersonation  | The server can impersonate the client's security context on the local system.                    |
| SecurityDelegation     | The server can impersonate the client's security context on remote systems.                      |



 

The client of a named pipe, RPC, or DDE connection can control the impersonation level. For example, a named pipe client can call the [**CreateFile**](https://msdn.microsoft.com/library/windows/desktop/aa363858) function to open a handle to a named pipe and specify the server's impersonation level.

When the named pipe, RPC, or DDE connection is remote, the flags passed to [**CreateFile**](https://msdn.microsoft.com/library/windows/desktop/aa363858) to set the impersonation level are ignored. In this case, the impersonation level of the client is determined by the impersonation levels enabled by the server, which is set by a flag on the server's account in the directory service. For example, if the server is enabled for delegation, the client's impersonation level will also be set to delegation even if the flags passed to **CreateFile** specify the identification impersonation level.

DDE clients use the [**DdeSetQualityOfService**](_win32_ddesetqualityofservice_cpp) function with the [**SECURITY\_QUALITY\_OF\_SERVICE**](security-quality-of-service.md) structure to specify the impersonation level. The SecurityImpersonation level is the default for named pipe, RPC, and DDE servers. The [**ImpersonateSelf**](impersonateself.md), [**DuplicateToken**](duplicatetoken.md), and [**DuplicateTokenEx**](duplicatetokenex.md) functions allow the caller to specify an impersonation level. Use the [**GetTokenInformation**](gettokeninformation.md) function to retrieve the impersonation level of an [*access token*](https://msdn.microsoft.com/library/windows/desktop/ms721532#-security-access-token-gly).

At the SecurityImpersonation level, most of the thread's actions occur in the security context of the thread's [*impersonation token*](https://msdn.microsoft.com/library/windows/desktop/ms721588#-security-impersonation-token-gly) rather than in the [*primary token*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-primary-token-gly) of the [*process*](https://msdn.microsoft.com/library/windows/desktop/ms721603#-security-process-gly) that owns the thread. For example, if an impersonating thread opens a [securable object](securable-objects.md), the system uses the impersonation token to check the thread's access. Similarly, if an impersonating thread creates a new object, for example by calling the [**CreateFile**](https://msdn.microsoft.com/library/windows/desktop/aa363858) function, the owner of the new object is the default owner from the client's [*access token*](https://msdn.microsoft.com/library/windows/desktop/ms721532#-security-access-token-gly).

However, the system uses the primary token of the process rather than the impersonation token of the calling thread in the following situations:

-   If an impersonating thread calls the [**CreateProcess**](https://msdn.microsoft.com/library/windows/desktop/ms682425) function, the new process always inherits the primary token of the process.
-   For functions that require the SE\_TCB\_NAME privilege, such as the [**LogonUser**](https://msdn.microsoft.com/library/windows/desktop/aa378184) function, the system always checks for the privilege in the primary token of the process.
-   For functions that require the SE\_AUDIT\_NAME privilege, such as the [**ObjectOpenAuditAlarm**](objectopenauditalarm.md) function, the system always checks for the privilege in the primary token of the process.
-   In a call to the [**OpenThreadToken**](openthreadtoken.md) function, a thread can specify whether the function uses the impersonation token or the primary token to determine whether to grant the requested access.

 

 


