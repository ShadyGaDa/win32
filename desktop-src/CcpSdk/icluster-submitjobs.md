---
Description: 'Adds one or more specified jobs to the scheduling queue.'
audience: developer
author: 'REDMOND\\danlep'
manager: 'REDMOND\\timlt'
ms.assetid: '5e147892-6ed0-4691-8e40-7af2ca324723'
ms.prod: 'windows-server-dev'
ms.technology: 'compute-cluster-pack'
ms.tgt_platform: multiple
title: 'ICluster::SubmitJobs method'
---

# ICluster::SubmitJobs method

Adds one or more specified jobs to the scheduling queue.

## Syntax


```C++
HRESULT SubmitJobs(
  [in]�����������IClusterEnumerable *jobIds,
  [in]�����������BSTR ��������������userName,
  [in]�����������BSTR ��������������password,
  [in]�����������VARIANT_BOOL ������isConsole,
  [in, optional]�long ��������������hwndParent
);
```



## Parameters

<dl> <dt>

*jobIds* \[in\]
</dt> <dd>

An [**IClusterEnumerable**](iclusterenumerable.md) interface that contains the identifiers of one or more jobs to submit. The [**ICluster::AddJob**](icluster-addjob.md) method returns this value. The variant type of each item in the collection is VT\_I4. Set the **lVal** member of the variant to the identifier.

</dd> <dt>

*userName* \[in\]
</dt> <dd>

The name of the RunAs user, in the form *domain*\\*user*. The user name is limited to 80 Unicode characters.

If *userName* is **NULL**, empty, or not valid, the cluster searches the calling user's credential cache for the credentials to use. If the cache contains only one credential, that credential is used. If the cache does not exist or contains multiple credentials, the user is prompted for the credentials.

</dd> <dt>

*password* \[in\]
</dt> <dd>

The RunAs user's password. The password is limited to 127 Unicode characters. If **NULL**, the method uses the cached credentials. See [**ICluster::SetCachedCredentials**](icluster-setcachedcredentials.md). If the credentials are not cached, the current user is prompted for the credentials. If the *isConsole* parameter is VARIANT\_TRUE, the user is prompted in the console window; otherwise, the standard credentials dialog box is used.

</dd> <dt>

*isConsole* \[in\]
</dt> <dd>

Set the value to VARIANT\_TRUE if the application is a console-mode application. Set the value to VARIANT\_FALSE if the application is a GUI application.

</dd> <dt>

*hwndParent* \[in, optional\]
</dt> <dd>

The handle to use as the parent window for the modal credentials dialog box. If 0, HWND\_DESKTOP is used. The handle is ignored if *isConsole* is VARIANT\_TRUE.

</dd> </dl>

## Return value

If the method succeeds, the return value is S\_OK. Otherwise, the return value is an error code. To get a description of the error, call the [**ICluster::get\_ErrorMessage**](icluster-get-errormessage.md) method.

## Remarks

If the operation succeeds, the status of the job is **JobStatus\_Queued**. The job moves to the **JobStatus\_Running** state when all required resources are available and the scheduler starts the job. Tasks are started in the order in which they were added to the job, except if there is a [dependency](itask-put-depend.md).

You can submit a job that does not contain tasks to reserve resources for the job. If the [**IJob::put\_RunUntilCanceled**](ijob-put-rununtilcanceled.md) method's *pRetVal* parameter is VARIANT\_TRUE, the job is scheduled and runs indefinitely or until it exceeds the run-time limit set in the [**IJob::put\_Runtime**](ijob-put-runtime.md) method (when the run-time value expires, the job is canceled). If the **put\_RunUntilCanceled** method's *pRetVal* parameter is VARIANT\_FALSE, the state of the job moves to the finished state.

If the method fails to submit one of the jobs, none of the jobs are submitted.

## Requirements



|                         |                                                                                       |
|-------------------------|---------------------------------------------------------------------------------------|
| Product<br/>      | Compute Cluster Pack Client Utilities<br/>                                      |
| Type library<br/> | <dl> <dt>Ccpapi.tlb</dt> </dl> |



## See also

<dl> <dt>

[**ICluster**](icluster.md)
</dt> <dt>

[**ICluster::SubmitJob**](icluster-submitjob.md)
</dt> <dt>

[**ICluster::QueueJobs**](icluster-queuejobs.md)
</dt> </dl>

�

�



