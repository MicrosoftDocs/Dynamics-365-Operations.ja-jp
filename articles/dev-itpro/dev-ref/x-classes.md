---
title: X クラス
description: 文字 X で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 55811
ms.assetid: bc7f3c76-9d89-4a32-a5c3-dfb783c4f4f3
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1617a2b313a45bf8eb06797c32535d563d82457b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369612"
---
# <a name="x-classes"></a>X クラス

[!include [banner](../includes/banner.md)]

文字 X で始まるシステム API クラス。

<a name="class-xapplication"></a>クラス xApplication
------------------

    class xApplication extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                                              | 説明                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean IsTablePerHierarchyMode()                                                                                                                                                                                            | すべてのテーブルの継承階層をフラットにしてシステムを実行するかどうかを決定します (階層ごとの表モード)。                                                         |
| public str buildNo()                                                                                                                                                                                                                |                                                                                                                                                                                 |
| public boolean canDeleteCompany(SelectableDataArea company)                                                                                                                                                                         |                                                                                                                                                                                 |
| public int countOfTopLevelFormsOpened()                                                                                                                                                                                             |                                                                                                                                                                                 |
| public Company company(\[SelectableDataArea company\])                                                                                                                                                                              |                                                                                                                                                                                 |
| public Int64 curTransactionId(\[boolean ForceTakeNumber\])                                                                                                                                                                          |                                                                                                                                                                                 |
| public boolean dbSynchronize(\[TableId tableId\], \[boolean checkAsNeeded\], \[boolean continueOnError\], \[boolean showProgress\], \[container checkSyncTables\], \[boolean createAllIndexes\], \[boolean useLockForSingleTable\]) |                                                                                                                                                                                 |
| public str getSameNameDifferentIdFields()                                                                                                                                                                                           |                                                                                                                                                                                 |
| public Map getServiceHostStatus()                                                                                                                                                                                                   |                                                                                                                                                                                 |
| public boolean isCheckedMode()                                                                                                                                                                                                      |                                                                                                                                                                                 |
| public boolean isConfigMode()                                                                                                                                                                                                       |                                                                                                                                                                                 |
| public boolean isDemoMode()                                                                                                                                                                                                         |                                                                                                                                                                                 |
| public boolean isSqlConnected()                                                                                                                                                                                                     |                                                                                                                                                                                 |
| public int numberOfTreeNodesLoaded()                                                                                                                                                                                                |                                                                                                                                                                                 |
| public str releaseVersion()                                                                                                                                                                                                         |                                                                                                                                                                                 |
| public boolean setDefaultCompany(SelectableDataArea company)                                                                                                                                                                        |                                                                                                                                                                                 |
| public int ttsLevel()                                                                                                                                                                                                               |                                                                                                                                                                                 |
| public int ttsVersion()                                                                                                                                                                                                             |                                                                                                                                                                                 |
| ::public static boolean CheckUserExistsInAnyPartition(str userId)                                                                                                                                                                   | 指定されたユーザーがどのパーティションにも存在するかどうかをチェックします。                                                                                                                      |
| ::public static str getFolderPath(int folder)                                                                                                                                                                                       |                                                                                                                                                                                 |
| ::public static str getVSAssembliesPath()                                                                                                                                                                                           |                                                                                                                                                                                 |
| ::public static boolean ilCacheContains(str owner, str key)                                                                                                                                                                         |                                                                                                                                                                                 |
| ::public static str ilCacheDelete(str owner, str key)                                                                                                                                                                               |                                                                                                                                                                                 |
| ::public static str ilCacheFind(str owner, str key)                                                                                                                                                                                 |                                                                                                                                                                                 |
| ::public static boolean initPartition(Partition partition)                                                                                                                                                                          | DAT 会社と管理者ユーザーを作成することで指定したパーティションを初期化します。                                                                                                   |
| ::public static boolean isServiceRegisteredOnClient(ClassId classId)                                                                                                                                                                |                                                                                                                                                                                 |
| ::public static boolean IsSinglePartitionSystem()                                                                                                                                                                                   | 配置が単一のパーティションか複数パーティションかを評価します。                                                                                                 |
| ::public static CLRObject XppILAppDomain()                                                                                                                                                                                          |                                                                                                                                                                                 |
| public boolean isInTransactionScope()                                                                                                                                                                                               |                                                                                                                                                                                 |
| public Int64 transactionScopeCommitLevel()                                                                                                                                                                                          |                                                                                                                                                                                 |
| public container Encrypt(str input)                                                                                                                                                                                                 |                                                                                                                                                                                 |
| public str Decrypt(container cipher)                                                                                                                                                                                                |                                                                                                                                                                                 |
| public System.Security.SecureString decryptToSecureString(container cipher)                                                                                                                                                         |                                                                                                                                                                                 |
| public container encryptFromSecureString(System.Security.SecureString input)                                                                                                                                                        |                                                                                                                                                                                 |
| public container EncryptForPurpose(str input, str purpose)                                                                                                                                                                          |                                                                                                                                                                                 |
| public str DecryptForPurpose(container cipher, str purpose)                                                                                                                                                                         |                                                                                                                                                                                 |
| public System.Security.SecureString decryptToSecureStringForPurpose(container cipher, str purpose)                                                                                                                                  |                                                                                                                                                                                 |
| public container encryptFromSecureStringForPurpose(System.Security.SecureString input, str purpose)                                                                                                                                 |                                                                                                                                                                                 |
| public str convertToUnsecureString(System.Security.SecureString secureString)                                                                                                                                                       |                                                                                                                                                                                 |
| public System.Security.SecureString convertToSecureString(str unsecureString)                                                                                                                                                       |                                                                                                                                                                                 |
| ::public static void startBatch()                                                                                                                                                                                                   |                                                                                                                                                                                 |
| public void deleteCompany(SelectableDataArea company)                                                                                                                                                                               |                                                                                                                                                                                 |
| public void ttsabort()                                                                                                                                                                                                              |                                                                                                                                                                                 |
| public void transactionScopeCommit()                                                                                                                                                                                                |                                                                                                                                                                                 |
| public void new()                                                                                                                                                                                                                   | xApplication クラスの新しいインスタンスを初期化します。                                                                                                                           |
| ::public static void stopBatch()                                                                                                                                                                                                    |                                                                                                                                                                                 |
| public void logRenameKey(Common recordOrig, Common recordUpdated, container changedFields)                                                                                                                                          |                                                                                                                                                                                 |
| public void startup(str startupCmd, str buildNumber)                                                                                                                                                                                |                                                                                                                                                                                 |
| public void RedirectToDashboard()                                                                                                                                                                                                   |                                                                                                                                                                                 |
| public void insertXReferences()                                                                                                                                                                                                     | 相互参照情報をデータベースに挿入する必要があるときに、フレームワークによって呼び出されます。                                                                              |
| public void logUpdate(Common recordOrig, Common recordUpdated, container changedFields)                                                                                                                                             |                                                                                                                                                                                 |
| public void setStartPage(\[SysUserInfoStartPage startpage\])                                                                                                                                                                        |                                                                                                                                                                                 |
| ::public static void ilCacheInsert(str owner, str key, str value)                                                                                                                                                                   |                                                                                                                                                                                 |
| public void clearManagedCaches()                                                                                                                                                                                                    |                                                                                                                                                                                 |
| public void eventDelete(Common recordDeleted)                                                                                                                                                                                       | そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが削除されたときにカーネルにより呼び出されるコールバックとして機能します。               |
| public void enableCountryContextFilter()                                                                                                                                                                                            | 現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を有効にします。  |
| public void setTheme(\[SysUserInfoTheme theme\])                                                                                                                                                                                    |                                                                                                                                                                                 |
| public void sysTrace(SysTraceType traceType, container traceInfo)                                                                                                                                                                   |                                                                                                                                                                                 |
| public void initGlobal(Info infoObject, VersionControl versionControlObject)                                                                                                                                                        |                                                                                                                                                                                 |
| public void transactionScopeRollback(Int64 commitLevel)                                                                                                                                                                             |                                                                                                                                                                                 |
| public void ttsbegin()                                                                                                                                                                                                              |                                                                                                                                                                                 |
| public void flushcompanycache(SelectableDataArea company)                                                                                                                                                                           |                                                                                                                                                                                 |
| public void logDelete(Common recordDeleted)                                                                                                                                                                                         |                                                                                                                                                                                 |
| ::public static void registerServiceOnClient(ClassId classId, str externalName)                                                                                                                                                     |                                                                                                                                                                                 |
| public void eventUpdate(Common recordOrig, Common recordUpdated, container changedFields)                                                                                                                                           | そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが更新されたときにカーネルにより呼び出されるコールバックとして機能します。               |
| public void transactionScopeBegin()                                                                                                                                                                                                 |                                                                                                                                                                                 |
| ::public static void checkForNewBatchJobs()                                                                                                                                                                                         |                                                                                                                                                                                 |
| public void disableCountryContextFilter()                                                                                                                                                                                           | 現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を無効にします。 |
| public void xref(str path, xRef x)                                                                                                                                                                                                  |                                                                                                                                                                                 |
| public void transactionScopeAbort()                                                                                                                                                                                                 |                                                                                                                                                                                 |
| public void eventRenameKey(Common recordOrig, Common recordUpdated, container changedFields)                                                                                                                                        | そのテーブル内のレコードを監視するようにカーネルが設定されていれば、主キーの名前が変更されたときにカーネルにより呼び出されるコールバックとして機能します。                     |
| public void flushClientPerformanceOptions()                                                                                                                                                                                         |                                                                                                                                                                                 |
| ::public static void flushClientServices()                                                                                                                                                                                          |                                                                                                                                                                                 |
| public void restartServiceHost()                                                                                                                                                                                                    |                                                                                                                                                                                 |
| public void updateXrefTreeNode(TreeNode treeNode)                                                                                                                                                                                   | さまざまなノード タイプの相互参照情報が更新されると、フレームワークによって呼び出されます。                                                                             |
| public void ttscommit()                                                                                                                                                                                                             |                                                                                                                                                                                 |
| public void RequestCompanyChange(\[DataAreaSysCompany company\])                                                                                                                                                                    |                                                                                                                                                                                 |
| public void finalize()                                                                                                                                                                                                              |                                                                                                                                                                                 |
| public void eventInsert(Common recordInserted)                                                                                                                                                                                      | そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが挿入されたときにカーネルにより呼び出されるコールバックとして機能します。              |
| public void ttsNotifyBegin()                                                                                                                                                                                                        |                                                                                                                                                                                 |
| public void closeAllForms()                                                                                                                                                                                                         |                                                                                                                                                                                 |
| public void ttsNotifyCommit()                                                                                                                                                                                                       |                                                                                                                                                                                 |
| public void ttsNotifyPreCommit()                                                                                                                                                                                                    |                                                                                                                                                                                 |
| public void ttsNotifyPostBegin()                                                                                                                                                                                                    |                                                                                                                                                                                 |
| public void ttsNotifyAbort()                                                                                                                                                                                                        |                                                                                                                                                                                 |
| public void setDensity(\[SysUserInfoDensity theme\])                                                                                                                                                                                |                                                                                                                                                                                 |
| public void logInsert(Common recordInserted)                                                                                                                                                                                        |                                                                                                                                                                                 |

### <a name="method-istableperhierarchymode"></a>メソッド IsTablePerHierarchyMode

すべてのテーブルの継承階層をフラットにしてシステムを実行するかどうかを決定します (階層ごとの表モード)。

    public boolean IsTablePerHierarchyMode()

#### <a name="return-value"></a>戻り値

システムが階層別テーブル モードで実行されている場合は true。それ以外の場合は、false。

### <a name="method-buildno"></a>メソッド buildNo

    public str buildNo()

#### <a name="return-value"></a>戻り値

### <a name="method-candeletecompany"></a>メソッド canDeleteCompany

    public boolean canDeleteCompany(SelectableDataArea company)

#### <a name="parameters"></a>パラメーター

会社  

#### <a name="return-value"></a>戻り値

### <a name="method-countoftoplevelformsopened"></a>メソッド countOfTopLevelFormsOpened

    public int countOfTopLevelFormsOpened()

#### <a name="return-value"></a>戻り値

### <a name="method-company"></a>メソッド company

    public Company company([SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

会社  

#### <a name="return-value"></a>戻り値

### <a name="method-curtransactionid"></a>メソッド curTransactionId

    public Int64 curTransactionId([boolean ForceTakeNumber])

#### <a name="parameters"></a>パラメーター

ForceTakeNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-dbsynchronize"></a>メソッド dbSynchronize

    public boolean dbSynchronize([TableId tableId], [boolean checkAsNeeded], [boolean continueOnError], [boolean showProgress], [container checkSyncTables], [boolean createAllIndexes], [boolean useLockForSingleTable])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

checkAsNeeded  

<!-- -->

continueOnError  

<!-- -->

showProgress  

<!-- -->

checkSyncTables  

<!-- -->

createAllIndexes  

<!-- -->

useLockForSingleTable  

#### <a name="return-value"></a>戻り値

### <a name="method-getsamenamedifferentidfields"></a>メソッド getSameNameDifferentIdFields

    public str getSameNameDifferentIdFields()

#### <a name="return-value"></a>戻り値

### <a name="method-getservicehoststatus"></a>メソッド getServiceHostStatus

    public Map getServiceHostStatus()

#### <a name="return-value"></a>戻り値

### <a name="method-ischeckedmode"></a>メソッド isCheckedMode

    public boolean isCheckedMode()

#### <a name="return-value"></a>戻り値

### <a name="method-isconfigmode"></a>メソッド isConfigMode

    public boolean isConfigMode()

#### <a name="return-value"></a>戻り値

### <a name="method-isdemomode"></a>メソッド isDemoMode

    public boolean isDemoMode()

#### <a name="return-value"></a>戻り値

### <a name="method-issqlconnected"></a>メソッド isSqlConnected

    public boolean isSqlConnected()

#### <a name="return-value"></a>戻り値

### <a name="method-numberoftreenodesloaded"></a>メソッド numberOfTreeNodesLoaded

    public int numberOfTreeNodesLoaded()

#### <a name="return-value"></a>戻り値

### <a name="method-releaseversion"></a>メソッド releaseVersion

    public str releaseVersion()

#### <a name="return-value"></a>戻り値

### <a name="method-setdefaultcompany"></a>メソッド setDefaultCompany

    public boolean setDefaultCompany(SelectableDataArea company)

#### <a name="parameters"></a>パラメーター

会社  

#### <a name="return-value"></a>戻り値

### <a name="method-ttslevel"></a>メソッド ttsLevel

    public int ttsLevel()

#### <a name="return-value"></a>戻り値

### <a name="method-ttsversion"></a>メソッド ttsVersion

    public int ttsVersion()

#### <a name="return-value"></a>戻り値

### <a name="method-checkuserexistsinanypartition"></a>メソッド CheckUserExistsInAnyPartition

指定されたユーザーがどのパーティションにも存在するかどうかをチェックします。

    public static boolean CheckUserExistsInAnyPartition(str userId)

#### <a name="parameters"></a>パラメーター

userId  

#### <a name="return-value"></a>戻り値

ユーザーがいずれかのパーティションに存在する場合は true。それ以外の場合は、false。

### <a name="method-getfolderpath"></a>メソッド getFolderPath

    public static str getFolderPath(int folder)

#### <a name="parameters"></a>パラメーター

folder  

#### <a name="return-value"></a>戻り値

### <a name="method-getvsassembliespath"></a>メソッド getVSAssembliesPath

    public static str getVSAssembliesPath()

#### <a name="return-value"></a>戻り値

### <a name="method-ilcachecontains"></a>メソッド ilCacheContains

    public static boolean ilCacheContains(str owner, str key)

#### <a name="parameters"></a>パラメーター

owner  

<!-- -->

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-ilcachedelete"></a>メソッド ilCacheDelete

    public static str ilCacheDelete(str owner, str key)

#### <a name="parameters"></a>パラメーター

owner  

<!-- -->

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-ilcachefind"></a>メソッド ilCacheFind

    public static str ilCacheFind(str owner, str key)

#### <a name="parameters"></a>パラメーター

owner  

<!-- -->

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-initpartition"></a>メソッド initPartition

DAT 会社と管理者ユーザーを作成することで指定したパーティションを初期化します。

    public static boolean initPartition(Partition partition)

#### <a name="parameters"></a>パラメーター

パーティション  
初期化するパーティションのレコード ID。

#### <a name="return-value"></a>戻り値

初期化が成功した場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

この API は、アップグレード フレームワークでのみ使用されます。 それを他のコンテキストで使用すると、データに回復不能な影響が発生することがあります。

### <a name="method-isserviceregisteredonclient"></a>メソッド isServiceRegisteredOnClient

    public static boolean isServiceRegisteredOnClient(ClassId classId)

#### <a name="parameters"></a>パラメーター

classId  

#### <a name="return-value"></a>戻り値

### <a name="method-issinglepartitionsystem"></a>メソッド IsSinglePartitionSystem

配置が単一のパーティションか複数パーティションかを評価します。

    public static boolean IsSinglePartitionSystem()

#### <a name="return-value"></a>戻り値

展開にパーティションが 1 つのみある場合は true。展開に複数のパーティションがある場合は false。

### <a name="method-xppilappdomain"></a>メソッド XppILAppDomain

    public static CLRObject XppILAppDomain()

#### <a name="return-value"></a>戻り値

### <a name="method-isintransactionscope"></a>メソッド isInTransactionScope

    public boolean isInTransactionScope()

#### <a name="return-value"></a>戻り値

### <a name="method-transactionscopecommitlevel"></a>メソッド transactionScopeCommitLevel

    public Int64 transactionScopeCommitLevel()

#### <a name="return-value"></a>戻り値

### <a name="method-encrypt"></a>メソッド Encrypt

    public container Encrypt(str input)

#### <a name="parameters"></a>パラメーター

input  

#### <a name="return-value"></a>戻り値

### <a name="method-decrypt"></a>メソッド Decrypt

    public str Decrypt(container cipher)

#### <a name="parameters"></a>パラメーター

cipher  

#### <a name="return-value"></a>戻り値

### <a name="method-decrypttosecurestring"></a>メソッド decryptToSecureString

    public System.Security.SecureString decryptToSecureString(container cipher)

#### <a name="parameters"></a>パラメーター

cipher  

#### <a name="return-value"></a>戻り値

### <a name="method-encryptfromsecurestring"></a>メソッド encryptFromSecureString

    public container encryptFromSecureString(System.Security.SecureString input)

#### <a name="parameters"></a>パラメーター

input  

#### <a name="return-value"></a>戻り値

### <a name="method-encryptforpurpose"></a>メソッド EncryptForPurpose

    public container EncryptForPurpose(str input, str purpose)

#### <a name="parameters"></a>パラメーター

input  

<!-- -->

purpose  

#### <a name="return-value"></a>戻り値

### <a name="method-decryptforpurpose"></a>メソッド DecryptForPurpose

    public str DecryptForPurpose(container cipher, str purpose)

#### <a name="parameters"></a>パラメーター

cipher  

<!-- -->

purpose  

#### <a name="return-value"></a>戻り値

### <a name="method-decrypttosecurestringforpurpose"></a>メソッド decryptToSecureStringForPurpose

    public System.Security.SecureString decryptToSecureStringForPurpose(container cipher, str purpose)

#### <a name="parameters"></a>パラメーター

cipher  

<!-- -->

purpose  

#### <a name="return-value"></a>戻り値

### <a name="method-encryptfromsecurestringforpurpose"></a>メソッド encryptFromSecureStringForPurpose

    public container encryptFromSecureStringForPurpose(System.Security.SecureString input, str purpose)

#### <a name="parameters"></a>パラメーター

input  

<!-- -->

purpose  

#### <a name="return-value"></a>戻り値

### <a name="method-converttounsecurestring"></a>メソッド convertToUnsecureString

    public str convertToUnsecureString(System.Security.SecureString secureString)

#### <a name="parameters"></a>パラメーター

secureString  

#### <a name="return-value"></a>戻り値

### <a name="method-converttosecurestring"></a>メソッド convertToSecureString

    public System.Security.SecureString convertToSecureString(str unsecureString)

#### <a name="parameters"></a>パラメーター

unsecureString  

#### <a name="return-value"></a>戻り値

### <a name="method-startbatch"></a>メソッド startBatch

    public static void startBatch()

### <a name="method-deletecompany"></a>メソッド deleteCompany

    public void deleteCompany(SelectableDataArea company)

#### <a name="parameters"></a>パラメーター

会社  

### <a name="method-ttsabort"></a>メソッド ttsabort

    public void ttsabort()

### <a name="method-transactionscopecommit"></a>メソッド transactionScopeCommit

    public void transactionScopeCommit()

### <a name="method-new"></a>メソッド new

xApplication クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-stopbatch"></a>メソッド stopBatch

    public static void stopBatch()

### <a name="method-logrenamekey"></a>メソッド logRenameKey

    public void logRenameKey(Common recordOrig, Common recordUpdated, container changedFields)

#### <a name="parameters"></a>パラメーター

recordOrig  

<!-- -->

recordUpdated  

<!-- -->

changedFields  

### <a name="method-startup"></a>メソッド startup

    public void startup(str startupCmd, str buildNumber)

#### <a name="parameters"></a>パラメーター

startupCmd  

<!-- -->

buildNumber  

### <a name="method-redirecttodashboard"></a>メソッド RedirectToDashboard

    public void RedirectToDashboard()

### <a name="method-insertxreferences"></a>メソッド insertXReferences

相互参照情報をデータベースに挿入する必要があるときに、フレームワークによって呼び出されます。

    public void insertXReferences()

#### <a name="remarks"></a>備考

Application クラスは、過負荷機能を提供します。

### <a name="method-logupdate"></a>メソッド logUpdate

    public void logUpdate(Common recordOrig, Common recordUpdated, container changedFields)

#### <a name="parameters"></a>パラメーター

recordOrig  

<!-- -->

recordUpdated  

<!-- -->

changedFields  

### <a name="method-setstartpage"></a>メソッド setStartPage

    public void setStartPage([SysUserInfoStartPage startpage])

#### <a name="parameters"></a>パラメーター

startpage  

### <a name="method-ilcacheinsert"></a>メソッド ilCacheInsert

    public static void ilCacheInsert(str owner, str key, str value)

#### <a name="parameters"></a>パラメーター

owner  

<!-- -->

キー  

<!-- -->

値  

### <a name="method-clearmanagedcaches"></a>メソッド clearManagedCaches

    public void clearManagedCaches()

### <a name="method-eventdelete"></a>メソッド eventDelete

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが削除されたときにカーネルにより呼び出されるコールバックとして機能します。

    public void eventDelete(Common recordDeleted)

#### <a name="parameters"></a>パラメーター

recordDeleted  
削除したレコード。

#### <a name="remarks"></a>備考

開発者は、特定のテーブルの削除時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実現できます。これには、logType フィールドを EventDelete に設定することが含まれます。 これは、logDelete メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、レコードが削除されたトランザクション内にあります。

### <a name="method-enablecountrycontextfilter"></a>メソッド enableCountryContextFilter

現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を有効にします。

    public void enableCountryContextFilter()

### <a name="method-settheme"></a>メソッド setTheme

    public void setTheme([SysUserInfoTheme theme])

#### <a name="parameters"></a>パラメーター

theme  

### <a name="method-systrace"></a>メソッド sysTrace

    public void sysTrace(SysTraceType traceType, container traceInfo)

#### <a name="parameters"></a>パラメーター

traceType  

<!-- -->

traceInfo  

### <a name="method-initglobal"></a>メソッド initGlobal

    public void initGlobal(Info infoObject, VersionControl versionControlObject)

#### <a name="parameters"></a>パラメーター

infoObject  

<!-- -->

versionControlObject  

### <a name="method-transactionscoperollback"></a>メソッド transactionScopeRollback

    public void transactionScopeRollback(Int64 commitLevel)

#### <a name="parameters"></a>パラメーター

commitLevel  

### <a name="method-ttsbegin"></a>メソッド ttsbegin

    public void ttsbegin()

### <a name="method-flushcompanycache"></a>メソッド flushcompanycache

    public void flushcompanycache(SelectableDataArea company)

#### <a name="parameters"></a>パラメーター

会社  

### <a name="method-logdelete"></a>メソッド logDelete

    public void logDelete(Common recordDeleted)

#### <a name="parameters"></a>パラメーター

recordDeleted  

### <a name="method-registerserviceonclient"></a>メソッド registerServiceOnClient

    public static void registerServiceOnClient(ClassId classId, str externalName)

#### <a name="parameters"></a>パラメーター

classId  

<!-- -->

externalName  

### <a name="method-eventupdate"></a>メソッド eventUpdate

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが更新されたときにカーネルにより呼び出されるコールバックとして機能します。

    public void eventUpdate(Common recordOrig, Common recordUpdated, container changedFields)

#### <a name="parameters"></a>パラメーター

recordOrig  
すべての変更されたフィールドのコンテナーです。

<!-- -->

recordUpdated  
すべての変更されたフィールドのコンテナーです。

<!-- -->

changedFields  
すべての変更されたフィールドのコンテナーです。

#### <a name="remarks"></a>備考

開発者は、特定のテーブルの更新時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventUpdate に設定することが含まれます。 レコードが更新されるとき、または特定のフィールドが更新されたときに必ず呼び出すカーネルを設定することができます。 これは、logUpdate メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、レコードが更新されたトランザクション内にあります。

### <a name="method-transactionscopebegin"></a>メソッド transactionScopeBegin

    public void transactionScopeBegin()

### <a name="method-checkfornewbatchjobs"></a>メソッド checkForNewBatchJobs

    public static void checkForNewBatchJobs()

### <a name="method-disablecountrycontextfilter"></a>メソッド disableCountryContextFilter

現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を無効にします。

    public void disableCountryContextFilter()

### <a name="method-xref"></a>メソッド xref

    public void xref(str path, xRef x)

#### <a name="parameters"></a>パラメーター

path  

<!-- -->

x  

### <a name="method-transactionscopeabort"></a>メソッド transactionScopeAbort

    public void transactionScopeAbort()

### <a name="method-eventrenamekey"></a>メソッド eventRenameKey

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、主キーの名前が変更されたときにカーネルにより呼び出されるコールバックとして機能します。

    public void eventRenameKey(Common recordOrig, Common recordUpdated, container changedFields)

#### <a name="parameters"></a>パラメーター

recordOrig  
すべての変更されたフィールドのコンテナーです。

<!-- -->

recordUpdated  
すべての変更されたフィールドのコンテナーです。

<!-- -->

changedFields  
すべての変更されたフィールドのコンテナーです。

#### <a name="remarks"></a>備考

開発者は、特定のテーブルの主キーの名前の変更時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventRenameKey に設定することが含まれます。 これは、logRenameKey メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、主キーの名前が変更されたトランザクションになります。

### <a name="method-flushclientperformanceoptions"></a>メソッド flushClientPerformanceOptions

    public void flushClientPerformanceOptions()

### <a name="method-flushclientservices"></a>メソッド flushClientServices

    public static void flushClientServices()

### <a name="method-restartservicehost"></a>メソッド restartServiceHost

    public void restartServiceHost()

### <a name="method-updatexreftreenode"></a>メソッド updateXrefTreeNode

さまざまなノード タイプの相互参照情報が更新されると、フレームワークによって呼び出されます。

    public void updateXrefTreeNode(TreeNode treeNode)

#### <a name="parameters"></a>パラメーター

treeNode  

#### <a name="remarks"></a>備考

Application クラスは、過負荷機能を提供します。

### <a name="method-ttscommit"></a>メソッド ttscommit

    public void ttscommit()

### <a name="method-requestcompanychange"></a>メソッド RequestCompanyChange

    public void RequestCompanyChange([DataAreaSysCompany company])

#### <a name="parameters"></a>パラメーター

会社  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-eventinsert"></a>メソッド eventInsert

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが挿入されたときにカーネルにより呼び出されるコールバックとして機能します。

    public void eventInsert(Common recordInserted)

#### <a name="parameters"></a>パラメーター

recordInserted  
挿入済みレコード。

#### <a name="remarks"></a>備考

開発者は、特定のテーブルの挿入時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventInsert に設定することが含まれます。 これは、logInsert メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、レコードが挿入されたトランザクション内にあります。

### <a name="method-ttsnotifybegin"></a>メソッド ttsNotifyBegin

    public void ttsNotifyBegin()

### <a name="method-closeallforms"></a>メソッド closeAllForms

    public void closeAllForms()

### <a name="method-ttsnotifycommit"></a>メソッド ttsNotifyCommit

    public void ttsNotifyCommit()

### <a name="method-ttsnotifyprecommit"></a>メソッド ttsNotifyPreCommit

    public void ttsNotifyPreCommit()

### <a name="method-ttsnotifypostbegin"></a>メソッド ttsNotifyPostBegin

    public void ttsNotifyPostBegin()

### <a name="method-ttsnotifyabort"></a>メソッド ttsNotifyAbort

    public void ttsNotifyAbort()

### <a name="method-setdensity"></a>メソッド setDensity

    public void setDensity([SysUserInfoDensity theme])

#### <a name="parameters"></a>パラメーター

theme  

### <a name="method-loginsert"></a>メソッド logInsert

    public void logInsert(Common recordInserted)

#### <a name="parameters"></a>パラメーター

recordInserted  

## <a name="class-xargs"></a>クラス xArgs
    class xArgs extends Object

xArgs クラスは、アプリケーション オブジェクト間の名前、呼び出し元、パラメーターなどの引数を渡すために使用されます。

### <a name="remarks"></a>備考

フォーム、レポートおよびクエリはすべてこのクラスを、コンストラクターで最初の引数として使用します。 このクラスを使用する適切な方法は、xArgs オブジェクトを作成し、名前文字列を指定してから、フォーム コンストラクタまたは ClassFactory メソッドに xArgs オブジェクトを渡すことです。 これらのクラスの中の 1 つに渡された xArgs オブジェクトを参照する場合は、そのクラスの args メソッドを使用してアクセスできます。 追加情報を新しいクラスに渡すために使用できるメソッドは 4 つあります。

-   parm - 文字列を渡すため
-   parmEnum および parmEnumType メソッド - 列挙値を渡すため
-   parmObject メソッド - 任意の型のオブジェクトを渡すため

呼び出し元から送信された xArgs クラスのインスタンスは、カーネルによって自動的に、または呼び出し元によって明示的に作成されます。 呼び出し元がメニュー項目を使用してオブジェクトを呼び出すとき、カーネル コードによって、xArgs クラスのインスタンスが作成されます。 メニュー項目名は、使用するメニュー項目の名前に設定されます。 メニュー項目に、EnumParameter、Parameters、EnumParameter、または EnumTypeParameter プロパティが設定されている場合、カーネルは xArgs クラスのこのインスタンスに対して Parm、ParmEnum、または ParmEnumType プロパティの値を設定します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                       | 説明                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| public boolean allowUseOfPreloadedForm(\[boolean value\])                                                    | このインスタンスに対して起動されたフォームが、プリロードされたフォーム プールから取得されたものかどうかを判定します。                                             |
| public int arrIdx(\[int value\])                                                                             |                                                                                                                                       |
| public Object caller(\[Object value\])                                                                       | xArgs クラスのこのインスタンスを作成したオブジェクトのインスタンスを取得または設定します。                                                |
| public IDispatcherProxy callerDispatcher()                                                                   |                                                                                                                                       |
| public FormControl callerFormControl(\[FormControl value\])                                                  |                                                                                                                                       |
| public str callerName()                                                                                      |                                                                                                                                       |
| public UtilElementType callerType()                                                                          |                                                                                                                                       |
| public Guid callerId()                                                                                       |                                                                                                                                       |
| public str clientId(\[str value\])                                                                           |                                                                                                                                       |
| public CopyCallerQuery copyCallerQuery(\[CopyCallerQuery value\])                                            |                                                                                                                                       |
| public TableId dataset()                                                                                     | 呼び出し元オブジェクトが動作しているテーブルのテーブル ID を取得します。                                                                 |
| public str designName(\[str value\])                                                                         | レポートまたはフォームでデザインを示す文字列を取得または設定します。                                                                    |
| public ExtendedTypeId extType(\[ExtendedTypeId edt\], \[int arrayIndex\])                                    |                                                                                                                                       |
| public FormViewOption formViewOption(\[FormViewOption value\])                                               |                                                                                                                                       |
| public InitialQueryParameter initialQuery(\[InitialQueryParameter initialQueryParameter\])                   |                                                                                                                                       |
| public FieldId lookupField(\[FieldId value\])                                                                | 指定されたレコードの検索に使用するテーブルのフィールド ID を取得または設定します。                                                            |
| public Common lookupRecord(\[Common value\])                                                                 | 指定されたテーブルのレコードを検索します。                                                                                                |
| public TableId lookupTable(\[TableId value\])                                                                |                                                                                                                                       |
| public str lookupValue(\[str value\])                                                                        | テーブルのフィールドで値を検索する LookupField メソッドで使用する文字列を取得または設定します。                                       |
| public str managedContentItemName(\[str value\])                                                             |                                                                                                                                       |
| public str menuItemName(\[str value\])                                                                       | アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前を取得または設定します。                                                        |
| public MenuItemType menuItemType(\[MenuItemType value\])                                                     | アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプを取得または設定します。                                                 |
| public MultiSelectionContext multiSelectionContext()                                                         |                                                                                                                                       |
| public str name(\[str value\])                                                                               | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。             |
| public Object object(\[Object value\])                                                                       | 新しいインスタンスを開く対象となるオブジェクトのアプリケーション名を取得および設定します。                                                    |
| public OpenMode openMode(\[OpenMode value\])                                                                 |                                                                                                                                       |
| public Int64 parentWnd(\[Int64 value\])                                                                      |                                                                                                                                       |
| public str parm(\[str value\])                                                                               | 呼び出されるオブジェクトのさまざまな情報を指定する文字列を取得または設定します。                                                 |
| public AnyType parmEnum(\[int value\])                                                                       | parmEnumType メソッドで指定されている列挙型の列挙値を取得または設定します。                              |
| public int parmEnumType(\[int value\])                                                                       | 任意の列挙タイプの ID 値を取得または設定します。                                                                                    |
| public Object parmObject(\[Object value\])                                                                   | 呼び出されるオブジェクトに渡す任意のオブジェクトのインスタンスを取得または設定します。                                                                 |
| public Common record(\[Common value\])                                                                       | 呼び出し元オブジェクトが動作しているテーブルのレコードを取得または設定します。                                                         |
| public FieldId refField(\[FieldId value\])                                                                   |                                                                                                                                       |
| public str getRequestContextQuery()                                                                          |                                                                                                                                       |
| public str requestContextQuery(str value)                                                                    |                                                                                                                                       |
| public FieldId selectField(\[FieldId value\])                                                                |                                                                                                                                       |
| public str toString()                                                                                        | xArgs のインスタンスの文字列形式を取得します。                                                                        |
| public boolean applyRecordAsDynalink(\[boolean applyAsDynalink\])                                            |                                                                                                                                       |
| public void onCallerChanged(\[Object value\])                                                                |                                                                                                                                       |
| public void new(\[AnyType nameOrCaller\], \[Object object\])                                                 | このクラスのインスタンスを構築します。このインスタンスは、FormRun クラスや ReportRun クラスなどの上位クラスに情報を渡すために使用されます。 |
| public void finalize()                                                                                       | メモリから xArgs クラスの現在のインスタンスを削除します。                                                                          |
| public void setupArgs(str parm, int enumType, AnyType enumValue, \[str menuItemName\], \[int menuItemType\]) |                                                                                                                                       |

### <a name="method-allowuseofpreloadedform"></a>メソッド allowUseOfPreloadedForm

このインスタンスに対して起動されたフォームが、プリロードされたフォーム プールから取得されたものかどうかを判定します。

    public boolean allowUseOfPreloadedForm([boolean value])

#### <a name="parameters"></a>パラメーター

値  
読み込まれたフォームがプリロードされたフォーム プールから取得できるかどうかを決定するブール値。

#### <a name="return-value"></a>戻り値

このインスタンスのために起動されるフォームが事前に読み込まれたフォーム プールから取得される可能性がある場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

事前に読み込まれているフォームの使用は、既定で許可されています。 事前に読み込まれたフォームを使用して悪影響があった場合にのみ、これを false に設定します。

### <a name="method-arridx"></a>メソッド arrIdx

    public int arrIdx([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-caller"></a>メソッド caller

xArgs クラスのこのインスタンスを作成したオブジェクトのインスタンスを取得または設定します。

    public Object caller([Object value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

呼び出し元オブジェクトの現在のインスタンス。

### <a name="method-callerdispatcher"></a>メソッド callerDispatcher

    public IDispatcherProxy callerDispatcher()

#### <a name="return-value"></a>戻り値

### <a name="method-callerformcontrol"></a>メソッド callerFormControl

    public FormControl callerFormControl([FormControl value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-callername"></a>メソッド callerName

    public str callerName()

#### <a name="return-value"></a>戻り値

### <a name="method-callertype"></a>メソッド callerType

    public UtilElementType callerType()

#### <a name="return-value"></a>戻り値

### <a name="method-callerid"></a>メソッド callerId

    public Guid callerId()

#### <a name="return-value"></a>戻り値

### <a name="method-clientid"></a>メソッド clientId

    public str clientId([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-copycallerquery"></a>メソッド copyCallerQuery

    public CopyCallerQuery copyCallerQuery([CopyCallerQuery value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dataset"></a>メソッド dataset

呼び出し元オブジェクトが動作しているテーブルのテーブル ID を取得します。

    public TableId dataset()

#### <a name="return-value"></a>戻り値

呼び出し元オブジェクトが動作しているテーブルのテーブル ID。

#### <a name="remarks"></a>備考

戻り値は、レコード メソッドで呼び出し元から転送されているレコードの種類を識別するために、頻繁に使用されます。

### <a name="method-designname"></a>メソッド designName

レポートまたはフォームでデザインを示す文字列を取得または設定します。

    public str designName([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

### <a name="method-exttype"></a>メソッド extType

    public ExtendedTypeId extType([ExtendedTypeId edt], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

edt  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-formviewoption"></a>メソッド formViewOption

    public FormViewOption formViewOption([FormViewOption value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-initialquery"></a>メソッド initialQuery

    public InitialQueryParameter initialQuery([InitialQueryParameter initialQueryParameter])

#### <a name="parameters"></a>パラメーター

initialQueryParameter  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupfield"></a>メソッド lookupField

指定されたレコードの検索に使用するテーブルのフィールド ID を取得または設定します。

    public FieldId lookupField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

指定されたレコードを検索するために使用するテーブル内のフィールドのフィールド ID。

#### <a name="remarks"></a>備考

戻り値は、呼び出されたオブジェクトが LookupRecord メソッド内の指定されたレコードまたは LookupValue メソッドで指定された文字列を検索するために、使用されます。 たとえば、以下を使用して検索するフィールドを設定することができます: xArgs.lookupField(fieldnum(TableName, FieldName));

### <a name="method-lookuprecord"></a>メソッド lookupRecord

指定されたテーブルのレコードを検索します。

    public Common lookupRecord([Common value])

#### <a name="parameters"></a>パラメーター

値  
レコードを検索するテーブル。

#### <a name="return-value"></a>戻り値

指定されたテーブルのレコード。

#### <a name="remarks"></a>備考

このメソッドは、呼び出されたオブジェクトが lookupField メソッドから返されるフィールド ID と組み合わせて使用され、このメソッドによって返されるレコード内のフィールドの値を検索します。

### <a name="method-lookuptable"></a>メソッド lookupTable

    public TableId lookupTable([TableId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupvalue"></a>メソッド lookupValue

テーブルのフィールドで値を検索する LookupField メソッドで使用する文字列を取得または設定します。

    public str lookupValue([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

LookupField メソッドで値を検索するために使用する文字列。

### <a name="method-managedcontentitemname"></a>メソッド managedContentItemName

    public str managedContentItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前を取得または設定します。

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前。

#### <a name="remarks"></a>備考

たとえば、メニュー項目を設定するには、以下を使用できます: xArgs.menuItemName(menuitemdisplaystr(CostingVersionPeriodic));

### <a name="method-menuitemtype"></a>メソッド menuItemType

アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプを取得または設定します。

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプ。

#### <a name="remarks"></a>備考

メニュー項目タイプは、表示、出力、またはアクションの列挙型のいずれかになります。

### <a name="method-multiselectioncontext"></a>メソッド multiSelectionContext

    public MultiSelectionContext multiSelectionContext()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることができます。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

たとえば、アプリケーション オブジェクトからフォームを呼び出すには、args.name(formstr(FormName)); を使用できます。

### <a name="method-object"></a>メソッド object

新しいインスタンスを開く対象となるオブジェクトのアプリケーション名を取得および設定します。

    public Object object([Object value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

新しいインスタンスを開く対象となるオブジェクトのアプリケーション名。

#### <a name="remarks"></a>備考

value パラメーターは、次のオブジェクトのいずれかのタイプである場合があります。

-   フォーム
-   レポート 
-   ジョブ
-   クラス
-   クエリ。

### <a name="method-openmode"></a>メソッド openMode

    public OpenMode openMode([OpenMode value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parentwnd"></a>メソッド parentWnd

    public Int64 parentWnd([Int64 value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parm"></a>メソッド parm

呼び出されるオブジェクトのさまざまな情報を指定する文字列を取得または設定します。

    public str parm([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

呼び出されるオブジェクトのさまざまな情報を指定する文字列の値。

### <a name="method-parmenum"></a>メソッド parmEnum

parmEnumType メソッドで指定されている列挙型の列挙値を取得または設定します。

    public AnyType parmEnum([int value])

#### <a name="parameters"></a>パラメーター

値  
設定する列挙型のキー。オプション。

#### <a name="return-value"></a>戻り値

parmEnumType メソッドで指定されている列挙型の列挙値。

#### <a name="remarks"></a>備考

このメソッドは、次の parmEnumType メソッドでよく使用されます: args.parmEnumType(enumnum(AssetBookType));args.parmEnumType(enumnum(AssetBookType));

### <a name="method-parmenumtype"></a>メソッド parmEnumType

任意の列挙タイプの ID 値を取得または設定します。

    public int parmEnumType([int value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

列挙型の ID 値。

#### <a name="remarks"></a>備考

このメソッドは、parmEnum メソッドとともに使用され、呼び出されたオブジェクトに列挙型の特定の値を送信します。 例: args.parmEnumType(enumnum(AssetBookType));args.parmEnum(AssetBookType::ValueModel);

### <a name="method-parmobject"></a>メソッド parmObject

呼び出されるオブジェクトに渡す任意のオブジェクトのインスタンスを取得または設定します。

    public Object parmObject([Object value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

呼び出されるオブジェクトに渡すオブジェクトのインスタンス。

#### <a name="remarks"></a>備考

オブジェクト多くの場合、クラスになります。

### <a name="method-record"></a>メソッド record

呼び出し元オブジェクトが動作しているテーブルのレコードを取得または設定します。

    public Common record([Common value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

呼び出し元オブジェクトが動作しているテーブルのレコード。

#### <a name="remarks"></a>備考

このメソッドは、呼び出し元のオブジェクトが現在使用しているレコードの値にアクセスするために使用されます。

### <a name="method-reffield"></a>メソッド refField

    public FieldId refField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getrequestcontextquery"></a>メソッド getRequestContextQuery

    public str getRequestContextQuery()

#### <a name="return-value"></a>戻り値

### <a name="method-requestcontextquery"></a>メソッド requestContextQuery

    public str requestContextQuery(str value)

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-selectfield"></a>メソッド selectField

    public FieldId selectField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

xArgs のインスタンスの文字列形式を取得します。

    public str toString()

#### <a name="return-value"></a>戻り値

xArgs クラスのインスタンスの説明を含む文字列。

### <a name="method-applyrecordasdynalink"></a>メソッド applyRecordAsDynalink

    public boolean applyRecordAsDynalink([boolean applyAsDynalink])

#### <a name="parameters"></a>パラメーター

applyAsDynalink  

#### <a name="return-value"></a>戻り値

### <a name="method-oncallerchanged"></a>メソッド onCallerChanged

    public void onCallerChanged([Object value])

#### <a name="parameters"></a>パラメーター

値  

### <a name="method-new"></a>メソッド new

このクラスのインスタンスを構築します。このインスタンスは、FormRun クラスや ReportRun クラスなどの上位クラスに情報を渡すために使用されます。

    public void new([AnyType nameOrCaller], [Object object])

#### <a name="parameters"></a>パラメーター

nameOrCaller  
オブジェクトの引数。オプション。 このパラメーターは、xArgs クラスのインスタンスを作成するために使用され、nameOrCaller パラメーターが呼び出し元の引数である場合に使用されます。

<!-- -->

オブジェクト  
オブジェクトの引数。オプション。 このパラメーターは、xArgs クラスのインスタンスを作成するために使用され、nameOrCaller パラメーターが呼び出し元の引数である場合に使用されます。

#### <a name="remarks"></a>備考

xArgs オブジェクトを作成するには、(呼び出し元、オブジェクト) のペアまたは Name 引数を指定します。 どちらの引数もオプションであり適切な方法を呼び出すことによって構築した後すべての値を設定することができます。

### <a name="method-finalize"></a>メソッド finalize

メモリから xArgs クラスの現在のインスタンスを削除します。

    public void finalize()

### <a name="method-setupargs"></a>メソッド setupArgs

    public void setupArgs(str parm, int enumType, AnyType enumValue, [str menuItemName], [int menuItemType])

#### <a name="parameters"></a>パラメーター

parm  

<!-- -->

enumType  

<!-- -->

enumValue  

<!-- -->

menuItemName  

<!-- -->

menuItemType  

## <a name="class-xaxaptauserdetails"></a>クラス xAxaptaUserDetails
    class xAxaptaUserDetails extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                           | 説明                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| public UserAccountType getAccountType(int index) |                                                             |
| public int getUserCount()                        |                                                             |
| public str getUserDomain(int index)              |                                                             |
| public str getUserLogin(int index)               |                                                             |
| public str getUserMail(int index)                |                                                             |
| public str getUserName(int index)                |                                                             |
| public str getUserSid(int index)                 |                                                             |
| public boolean isUserEnabled(int index)          |                                                             |
| public boolean isUserExternal(int index)         |                                                             |
| public void finalize()                           |                                                             |
| public void new()                                | xAxaptaUserDetails クラスの新しいインスタンスを初期化します。 |

### <a name="method-getaccounttype"></a>メソッド getAccountType

    public UserAccountType getAccountType(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getusercount"></a>メソッド getUserCount

    public int getUserCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getuserdomain"></a>メソッド getUserDomain

    public str getUserDomain(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getuserlogin"></a>メソッド getUserLogin

    public str getUserLogin(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getusermail"></a>メソッド getUserMail

    public str getUserMail(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getusername"></a>メソッド getUserName

    public str getUserName(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getusersid"></a>メソッド getUserSid

    public str getUserSid(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-isuserenabled"></a>メソッド isUserEnabled

    public boolean isUserEnabled(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-isuserexternal"></a>メソッド isUserExternal

    public boolean isUserExternal(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

xAxaptaUserDetails クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-xaxaptausermanager"></a>クラス xAxaptaUserManager
    class xAxaptaUserManager extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                               | 説明                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| public container enumerateDomains(str server)                                                        |                                                                        |
| public xAxaptaUserDetails enumerateDomainUsers(str domainName)                                       |                                                                        |
| public str generatePassword()                                                                        |                                                                        |
| public xAxaptaUserDetails getDomainUser(str domainName, str userLogin)                               |                                                                        |
| public str getFQDN(str domainName, \[boolean throwError\])                                           |                                                                        |
| public container getGroupsForUser(str userName)                                                      |                                                                        |
| public container getRolesForUser(str userName, str company)                                          | 特定のユーザーのロールを取得します。                                         |
| public xAxaptaUserDetails getSIDFromName(str userLogin, str domainName, UserAccountType accountType) | 特定のユーザー ログオン、ドメイン、および勘定タイプからのユーザーの詳細を取得します。 |
| public str getUserSid(str username, str domain)                                                      |                                                                        |
| public boolean validateDomain(str domain)                                                            |                                                                        |
| public boolean validateOrgUnit(str ouName)                                                           |                                                                        |
| public boolean validatePassword(str username, str domain, str password)                              |                                                                        |
| public boolean validateSecGroup(str secGroup)                                                        |                                                                        |
| public void new()                                                                                    | xAxaptaUserManager クラスの新しいインスタンスを初期化します。            |
| public void updateUserRoleAssignments(UserId userId, container roles, container removeRoles)         |                                                                        |
| public void finalize()                                                                               |                                                                        |

### <a name="method-enumeratedomains"></a>メソッド enumerateDomains

    public container enumerateDomains(str server)

#### <a name="parameters"></a>パラメーター

server  

#### <a name="return-value"></a>戻り値

### <a name="method-enumeratedomainusers"></a>メソッド enumerateDomainUsers

    public xAxaptaUserDetails enumerateDomainUsers(str domainName)

#### <a name="parameters"></a>パラメーター

domainName  

#### <a name="return-value"></a>戻り値

### <a name="method-generatepassword"></a>メソッド generatePassword

    public str generatePassword()

#### <a name="return-value"></a>戻り値

### <a name="method-getdomainuser"></a>メソッド getDomainUser

    public xAxaptaUserDetails getDomainUser(str domainName, str userLogin)

#### <a name="parameters"></a>パラメーター

domainName  

<!-- -->

userLogin  

#### <a name="return-value"></a>戻り値

### <a name="method-getfqdn"></a>メソッド getFQDN

    public str getFQDN(str domainName, [boolean throwError])

#### <a name="parameters"></a>パラメーター

domainName  

<!-- -->

throwError  

#### <a name="return-value"></a>戻り値

### <a name="method-getgroupsforuser"></a>メソッド getGroupsForUser

    public container getGroupsForUser(str userName)

#### <a name="parameters"></a>パラメーター

userName  

#### <a name="return-value"></a>戻り値

### <a name="method-getrolesforuser"></a>メソッド getRolesForUser

特定のユーザーのロールを取得します。

    public container getRolesForUser(str userName, str company)

#### <a name="parameters"></a>パラメーター

userName  

<!-- -->

会社  

#### <a name="return-value"></a>戻り値

特定のユーザーのロールを保持するコンテナーです。

### <a name="method-getsidfromname"></a>メソッド getSIDFromName

特定のユーザー ログオン、ドメイン、および勘定タイプからのユーザーの詳細を取得します。

    public xAxaptaUserDetails getSIDFromName(str userLogin, str domainName, UserAccountType accountType)

#### <a name="parameters"></a>パラメーター

userLogin  

<!-- -->

domainName  

<!-- -->

accountType  

#### <a name="return-value"></a>戻り値

ユーザーの詳細を含む xAxaptaUserDetails クラス インスタンス。

### <a name="method-getusersid"></a>メソッド getUserSid

    public str getUserSid(str username, str domain)

#### <a name="parameters"></a>パラメーター

username  

<!-- -->

domain  

#### <a name="return-value"></a>戻り値

### <a name="method-validatedomain"></a>メソッド validateDomain

    public boolean validateDomain(str domain)

#### <a name="parameters"></a>パラメーター

domain  

#### <a name="return-value"></a>戻り値

### <a name="method-validateorgunit"></a>メソッド validateOrgUnit

    public boolean validateOrgUnit(str ouName)

#### <a name="parameters"></a>パラメーター

ouName  

#### <a name="return-value"></a>戻り値

### <a name="method-validatepassword"></a>メソッド validatePassword

    public boolean validatePassword(str username, str domain, str password)

#### <a name="parameters"></a>パラメーター

username  

<!-- -->

domain  

<!-- -->

パスワード  

#### <a name="return-value"></a>戻り値

### <a name="method-validatesecgroup"></a>メソッド validateSecGroup

    public boolean validateSecGroup(str secGroup)

#### <a name="parameters"></a>パラメーター

secGroup  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

xAxaptaUserManager クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-updateuserroleassignments"></a>メソッド updateUserRoleAssignments

    public void updateUserRoleAssignments(UserId userId, container roles, container removeRoles)

#### <a name="parameters"></a>パラメーター

userId  

<!-- -->

ロール  

<!-- -->

removeRoles  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-xbrowser"></a>クラス xBrowser
    class xBrowser extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                       | 説明 |
|----------------------------------------------------------------------------------------------|-------------|
| public void navigate(str downloadUrl, \[boolean openInNewTab\], \[boolean showExitWarning\]) |             |
| public void new()                                                                            |             |

### <a name="method-navigate"></a>メソッド navigate

    public void navigate(str downloadUrl, [boolean openInNewTab], [boolean showExitWarning])

#### <a name="parameters"></a>パラメーター

downloadUrl  

<!-- -->

openInNewTab  

<!-- -->

showExitWarning  

### <a name="method-new"></a>メソッド new

    public void new()

## <a name="class-xclassfactory"></a>クラス xClassFactory
    class xClassFactory extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                               | 説明                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| public xFormRun createAutoReportForm(xArgs args)                                                                                                     |                                                        |
| public xFormRun createLabelForm(xArgs args)                                                                                                          |                                                        |
| public xFormRun createRecInfoForm(xArgs args)                                                                                                        |                                                        |
| public ReportViewer createReportViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, \[ReportRun reportRun\])                                |                                                        |
| public xFormRun createSetupForm(xArgs args)                                                                                                          |                                                        |
| public ReportOutputUser createViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, ReportOutputUserType viewerType, \[ReportRun reportRun\]) |                                                        |
| public Object createWebPageEditor()                                                                                                                  |                                                        |
| public xFormRun formRunClass(xArgs args)                                                                                                             |                                                        |
| public container lastValueGet(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])               |                                                        |
| public QueryRun queryRunClass(xArgs args)                                                                                                            |                                                        |
| public ReportRun reportRunClass(xArgs args)                                                                                                          |                                                        |
| public Object startAOTWizard(TreeNode parent)                                                                                                        |                                                        |
| public void projectDeleted(str projectName)                                                                                                          |                                                        |
| public void lastValueDelete(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])                 |                                                        |
| public void lastValuePut(container value, SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])   |                                                        |
| public void drillDown(OutputField outputField, MenuItemType menuItemType, str menuItemName)                                                          |                                                        |
| public void new()                                                                                                                                    | xClassFactory クラスの新しいインスタンスを初期化します。 |

### <a name="method-createautoreportform"></a>メソッド createAutoReportForm

    public xFormRun createAutoReportForm(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

#### <a name="return-value"></a>戻り値

### <a name="method-createlabelform"></a>メソッド createLabelForm

    public xFormRun createLabelForm(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

#### <a name="return-value"></a>戻り値

### <a name="method-createrecinfoform"></a>メソッド createRecInfoForm

    public xFormRun createRecInfoForm(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

#### <a name="return-value"></a>戻り値

### <a name="method-createreportviewer"></a>メソッド createReportViewer

    public ReportViewer createReportViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, [ReportRun reportRun])

#### <a name="parameters"></a>パラメーター

jobsCursor  

<!-- -->

pagesCursor  

<!-- -->

reportRun  

#### <a name="return-value"></a>戻り値

### <a name="method-createsetupform"></a>メソッド createSetupForm

    public xFormRun createSetupForm(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

#### <a name="return-value"></a>戻り値

### <a name="method-createviewer"></a>メソッド createViewer

    public ReportOutputUser createViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, ReportOutputUserType viewerType, [ReportRun reportRun])

#### <a name="parameters"></a>パラメーター

jobsCursor  

<!-- -->

pagesCursor  

<!-- -->

viewerType  

<!-- -->

reportRun  

#### <a name="return-value"></a>戻り値

### <a name="method-createwebpageeditor"></a>メソッド createWebPageEditor

    public Object createWebPageEditor()

#### <a name="return-value"></a>戻り値

### <a name="method-formrunclass"></a>メソッド formRunClass

    public xFormRun formRunClass(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

#### <a name="return-value"></a>戻り値

### <a name="method-lastvalueget"></a>メソッド lastValueGet

    public container lastValueGet(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])

#### <a name="parameters"></a>パラメーター

会社  

<!-- -->

ユーザー  

<!-- -->

utilType  

<!-- -->

名前  

<!-- -->

design  

#### <a name="return-value"></a>戻り値

### <a name="method-queryrunclass"></a>メソッド queryRunClass

    public QueryRun queryRunClass(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

#### <a name="return-value"></a>戻り値

### <a name="method-reportrunclass"></a>メソッド reportRunClass

    public ReportRun reportRunClass(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

#### <a name="return-value"></a>戻り値

### <a name="method-startaotwizard"></a>メソッド startAOTWizard

    public Object startAOTWizard(TreeNode parent)

#### <a name="parameters"></a>パラメーター

parent  

#### <a name="return-value"></a>戻り値

### <a name="method-projectdeleted"></a>メソッド projectDeleted

    public void projectDeleted(str projectName)

#### <a name="parameters"></a>パラメーター

projectName  

### <a name="method-lastvaluedelete"></a>メソッド lastValueDelete

    public void lastValueDelete(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])

#### <a name="parameters"></a>パラメーター

会社  

<!-- -->

ユーザー  

<!-- -->

utilType  

<!-- -->

名前  

<!-- -->

design  

### <a name="method-lastvalueput"></a>メソッド lastValuePut

    public void lastValuePut(container value, SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

会社  

<!-- -->

ユーザー  

<!-- -->

utilType  

<!-- -->

名前  

<!-- -->

design  

### <a name="method-drilldown"></a>メソッド drillDown

    public void drillDown(OutputField outputField, MenuItemType menuItemType, str menuItemName)

#### <a name="parameters"></a>パラメーター

outputField  

<!-- -->

menuItemType  

<!-- -->

menuItemName  

### <a name="method-new"></a>メソッド new

xClassFactory クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-xclasstrace"></a>クラス xClassTrace
    class xClassTrace extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                                                                                                                                                             | 説明                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| ::public static boolean isTracingEnabled(\[Int64 keyword\], \[int level\])                                                                                                         |                                                      |
| ::public static boolean isTracingStarted()                                                                                                                                         |                                                      |
| ::public static str kernelCustomerId()                                                                                                                                             |                                                      |
| ::public static Guid kernelRequestId()                                                                                                                                             |                                                      |
| ::public static str kernelSessionId()                                                                                                                                              |                                                      |
| ::public static str kernelUserId()                                                                                                                                                 |                                                      |
| ::public static int start(str logFileName, \[int logBufferSize\], \[int minBuffers\], \[int maxBuffers\], \[Int64 keywords\], \[int maxFileSize\], \[boolean useCircularLogging\]) |                                                      |
| ::public static int stop()                                                                                                                                                         |                                                      |
| ::public static void logMessage(str message)                                                                                                                                       |                                                      |
| public void endMarker(str transactionName)                                                                                                                                         |                                                      |
| public void beginMarker(str transactionName)                                                                                                                                       |                                                      |
| ::public static void logComponentMessage(str component, str message)                                                                                                               |                                                      |
| public void finalize()                                                                                                                                                             |                                                      |
| public void new()                                                                                                                                                                  | xClassTrace クラスの新しいインスタンスを初期化します。 |

### <a name="method-istracingenabled"></a>メソッド isTracingEnabled

    public static boolean isTracingEnabled([Int64 keyword], [int level])

#### <a name="parameters"></a>パラメーター

キーワード  

<!-- -->

level  

#### <a name="return-value"></a>戻り値

### <a name="method-istracingstarted"></a>メソッド isTracingStarted

    public static boolean isTracingStarted()

#### <a name="return-value"></a>戻り値

### <a name="method-kernelcustomerid"></a>メソッド kernelCustomerId

    public static str kernelCustomerId()

#### <a name="return-value"></a>戻り値

### <a name="method-kernelrequestid"></a>メソッド kernelRequestId

    public static Guid kernelRequestId()

#### <a name="return-value"></a>戻り値

### <a name="method-kernelsessionid"></a>メソッド kernelSessionId

    public static str kernelSessionId()

#### <a name="return-value"></a>戻り値

### <a name="method-kerneluserid"></a>メソッド kernelUserId

    public static str kernelUserId()

#### <a name="return-value"></a>戻り値

### <a name="method-start"></a>メソッド start

    public static int start(str logFileName, [int logBufferSize], [int minBuffers], [int maxBuffers], [Int64 keywords], [int maxFileSize], [boolean useCircularLogging])

#### <a name="parameters"></a>パラメーター

logFileName  

<!-- -->

logBufferSize  

<!-- -->

minBuffers  

<!-- -->

maxBuffers  

<!-- -->

keywords  

<!-- -->

maxFileSize  

<!-- -->

useCircularLogging  

#### <a name="return-value"></a>戻り値

### <a name="method-stop"></a>メソッド stop

    public static int stop()

#### <a name="return-value"></a>戻り値

### <a name="method-logmessage"></a>メソッド logMessage

    public static void logMessage(str message)

#### <a name="parameters"></a>パラメーター

メッセージ  

### <a name="method-endmarker"></a>メソッド endMarker

    public void endMarker(str transactionName)

#### <a name="parameters"></a>パラメーター

transactionName  

### <a name="method-beginmarker"></a>メソッド beginMarker

    public void beginMarker(str transactionName)

#### <a name="parameters"></a>パラメーター

transactionName  

### <a name="method-logcomponentmessage"></a>メソッド logComponentMessage

    public static void logComponentMessage(str component, str message)

#### <a name="parameters"></a>パラメーター

コンポーネント  

<!-- -->

メッセージ  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

xClassTrace クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-xcompany"></a>クラス xCompany
    class xCompany extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                              | 説明                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| public DataAreaId dataArea(TableId tableId)                                         |                                                    |
| public SelectableDataArea ext()                                                     |                                                    |
| public boolean log(DatabaseLogType typeOfLog, TableId tableId, \[FieldId fieldId\]) |                                                    |
| public boolean logAlways(DatabaseLogType typeOfLog, \[boolean log\])                | システム以外のテーブルのログを有効または無効にします。 |
| public boolean reindex(\[TableId tableId\])                                         |                                                    |
| public void reloadLog()                                                             |                                                    |
| public void new(SelectableDataArea company)                                         | Object クラスの新しいインスタンスを初期化します。    |
| public void check()                                                                 |                                                    |
| public void reloadRights()                                                          |                                                    |
| public void flushCache(TableId tableId)                                             |                                                    |
| public void reloadTableCollections()                                                |                                                    |

### <a name="method-dataarea"></a>メソッド dataArea

    public DataAreaId dataArea(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

#### <a name="return-value"></a>戻り値

### <a name="method-ext"></a>メソッド ext

    public SelectableDataArea ext()

#### <a name="return-value"></a>戻り値

### <a name="method-log"></a>メソッド log

    public boolean log(DatabaseLogType typeOfLog, TableId tableId, [FieldId fieldId])

#### <a name="parameters"></a>パラメーター

typeOfLog  

<!-- -->

tableId  

<!-- -->

fieldId  

#### <a name="return-value"></a>戻り値

### <a name="method-logalways"></a>メソッド logAlways

システム以外のテーブルのログを有効または無効にします。

    public boolean logAlways(DatabaseLogType typeOfLog, [boolean log])

#### <a name="parameters"></a>パラメーター

typeOfLog  

<!-- -->

ログ  

#### <a name="return-value"></a>戻り値

呼び出し前の指定された操作のデータベース ロギングの状況。

#### <a name="remarks"></a>備考

オプションの typeOfLog パラメーターがない場合、このメソッドは指定されたオペレーションのデータベース ログの状態をレポートします。 オプションのパラメーターを指定する場合は、メソッドは CAS で保護されており、呼び出しコードは SysDatabaselogPermission をアサートする必要があることに注意してください。

### <a name="method-reindex"></a>メソッド reindex

    public boolean reindex([TableId tableId])

#### <a name="parameters"></a>パラメーター

tableId  

#### <a name="return-value"></a>戻り値

### <a name="method-reloadlog"></a>メソッド reloadLog

    public void reloadLog()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(SelectableDataArea company)

#### <a name="parameters"></a>パラメーター

会社  

### <a name="method-check"></a>メソッド check

    public void check()

### <a name="method-reloadrights"></a>メソッド reloadRights

    public void reloadRights()

### <a name="method-flushcache"></a>メソッド flushCache

    public void flushCache(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

### <a name="method-reloadtablecollections"></a>メソッド reloadTableCollections

    public void reloadTableCollections()

## <a name="class-xcompileroutput"></a>クラス xCompilerOutput
    class xCompilerOutput extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                         | 説明                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| public str getErrorMessage(int errorCode, int severity, str errorString)                                                       |                                                          |
| public container getSquiggleInfo(str treeNodePath)                                                                             |                                                          |
| public void compilerStatus(UtilElementType utilElementType, str utilElementName)                                               |                                                          |
| public void setActiveTab(int tab)                                                                                              |                                                          |
| public void startCompilationObject(str path)                                                                                   |                                                          |
| public void endCompilation()                                                                                                   |                                                          |
| public void startExport()                                                                                                      |                                                          |
| public void startCompilation(int flag, str path, int activeWindowHandle)                                                       |                                                          |
| public void importOutput(str buffer)                                                                                           |                                                          |
| public void endExport()                                                                                                        |                                                          |
| public void endCompilationObject(str path)                                                                                     |                                                          |
| public void startImport()                                                                                                      |                                                          |
| public void new()                                                                                                              | xCompilerOutput クラスの新しいインスタンスを初期化します。 |
| public void compilerOutputMessage(str path, int errorCode, int line, int col, int severity, str errorString, str propertyName) |                                                          |
| public void exportOutput(str buffer)                                                                                           |                                                          |
| public void endCILGenerationOutput()                                                                                           |                                                          |
| public void cilGenerationOutput(str msg, str path, int severity, int line, int col)                                            |                                                          |
| public void endImport()                                                                                                        |                                                          |
| public void nextError()                                                                                                        |                                                          |
| public void startCILGenerationOutput()                                                                                         |                                                          |

### <a name="method-geterrormessage"></a>メソッド getErrorMessage

    public str getErrorMessage(int errorCode, int severity, str errorString)

#### <a name="parameters"></a>パラメーター

errorCode  

<!-- -->

severity  

<!-- -->

errorString  

#### <a name="return-value"></a>戻り値

### <a name="method-getsquiggleinfo"></a>メソッド getSquiggleInfo

    public container getSquiggleInfo(str treeNodePath)

#### <a name="parameters"></a>パラメーター

treeNodePath  

#### <a name="return-value"></a>戻り値

### <a name="method-compilerstatus"></a>メソッド compilerStatus

    public void compilerStatus(UtilElementType utilElementType, str utilElementName)

#### <a name="parameters"></a>パラメーター

utilElementType  

<!-- -->

utilElementName  

### <a name="method-setactivetab"></a>メソッド setActiveTab

    public void setActiveTab(int tab)

#### <a name="parameters"></a>パラメーター

tab  

### <a name="method-startcompilationobject"></a>メソッド startCompilationObject

    public void startCompilationObject(str path)

#### <a name="parameters"></a>パラメーター

path  

### <a name="method-endcompilation"></a>メソッド endCompilation

    public void endCompilation()

### <a name="method-startexport"></a>メソッド startExport

    public void startExport()

### <a name="method-startcompilation"></a>メソッド startCompilation

    public void startCompilation(int flag, str path, int activeWindowHandle)

#### <a name="parameters"></a>パラメーター

flag  

<!-- -->

path  

<!-- -->

activeWindowHandle  

### <a name="method-importoutput"></a>メソッド importOutput

    public void importOutput(str buffer)

#### <a name="parameters"></a>パラメーター

バッファ  

### <a name="method-endexport"></a>メソッド endExport

    public void endExport()

### <a name="method-endcompilationobject"></a>メソッド endCompilationObject

    public void endCompilationObject(str path)

#### <a name="parameters"></a>パラメーター

path  

### <a name="method-startimport"></a>メソッド startImport

    public void startImport()

### <a name="method-new"></a>メソッド new

xCompilerOutput クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-compileroutputmessage"></a>メソッド compilerOutputMessage

    public void compilerOutputMessage(str path, int errorCode, int line, int col, int severity, str errorString, str propertyName)

#### <a name="parameters"></a>パラメーター

path  

<!-- -->

errorCode  

<!-- -->

明細行  

<!-- -->

col  

<!-- -->

severity  

<!-- -->

errorString  

<!-- -->

propertyName  

### <a name="method-exportoutput"></a>メソッド exportOutput

    public void exportOutput(str buffer)

#### <a name="parameters"></a>パラメーター

バッファ  

### <a name="method-endcilgenerationoutput"></a>メソッド endCILGenerationOutput

    public void endCILGenerationOutput()

### <a name="method-cilgenerationoutput"></a>メソッド cilGenerationOutput

    public void cilGenerationOutput(str msg, str path, int severity, int line, int col)

#### <a name="parameters"></a>パラメーター

msg  

<!-- -->

path  

<!-- -->

severity  

<!-- -->

明細行  

<!-- -->

col  

### <a name="method-endimport"></a>メソッド endImport

    public void endImport()

### <a name="method-nexterror"></a>メソッド nextError

    public void nextError()

### <a name="method-startcilgenerationoutput"></a>メソッド startCILGenerationOutput

    public void startCILGenerationOutput()

## <a name="class-xdsservices"></a>クラス XDSServices
    class XDSServices extends Object

XDSServices クラスは、拡張可能なデータ セキュリティ (XDS) 動作を管理するための API を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                 | 説明                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public int flushXDSMyConstructs(int reserved, str tablename)           | XDS で使用される MyConstruct テーブルをフラッシュします。                                                                              |
| public str getQuerySQL(str queryname)                                  |                                                                                                                                   |
| public str getTableSQL(str tablename, \[str policyname\])              |                                                                                                                                   |
| public str getXDSBinding(str name)                                     |                                                                                                                                   |
| public str getXDSContext(int reserved)                                 |                                                                                                                                   |
| public int getXDSToFlushPerServiceSession(int reserved)                | サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかをチェックします。                           |
| public void finalize()                                                 |                                                                                                                                   |
| public void new()                                                      | XDSServices クラスの新しいインスタンスを初期化します。                                                                              |
| public void setXDSContext(int reserved, str contextstring)             |                                                                                                                                   |
| public void setXDSBinding(str name, str value)                         |                                                                                                                                   |
| public void setXDSState(int finalState)                                |                                                                                                                                   |
| public void setXDSToFlushPerServiceSession(int reserved, int newstate) | サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかを決定する設定を設定します。 |
| public void setXDSTrace(int flag, str value)                           |                                                                                                                                   |

### <a name="method-flushxdsmyconstructs"></a>メソッド flushXDSMyConstructs

XDS で使用される MyConstruct テーブルをフラッシュします。

    public int flushXDSMyConstructs(int reserved, str tablename)

#### <a name="parameters"></a>パラメーター

reserved  
フラッシュする MyConstruct テーブルの名前。 値が渡されない場合、または空の文字列が渡される場合、すべての MyConstruct テーブルがフラッシュされます。

<!-- -->

tablename  
フラッシュする MyConstruct テーブルの名前。 値が渡されない場合、または空の文字列が渡される場合、すべての MyConstruct テーブルがフラッシュされます。

#### <a name="return-value"></a>戻り値

### <a name="method-getquerysql"></a>メソッド getQuerySQL

    public str getQuerySQL(str queryname)

#### <a name="parameters"></a>パラメーター

queryname  

#### <a name="return-value"></a>戻り値

### <a name="method-gettablesql"></a>メソッド getTableSQL

    public str getTableSQL(str tablename, [str policyname])

#### <a name="parameters"></a>パラメーター

tablename  

<!-- -->

policyname  

#### <a name="return-value"></a>戻り値

### <a name="method-getxdsbinding"></a>メソッド getXDSBinding

    public str getXDSBinding(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-getxdscontext"></a>メソッド getXDSContext

    public str getXDSContext(int reserved)

#### <a name="parameters"></a>パラメーター

reserved  

#### <a name="return-value"></a>戻り値

### <a name="method-getxdstoflushperservicesession"></a>メソッド getXDSToFlushPerServiceSession

サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかをチェックします。

    public int getXDSToFlushPerServiceSession(int reserved)

#### <a name="parameters"></a>パラメーター

reserved  
予約済フラグ、現在使用されていません。

#### <a name="return-value"></a>戻り値

サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされる場合は 1、それ以外の場合は 0 です。

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

XDSServices クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-setxdscontext"></a>メソッド setXDSContext

    public void setXDSContext(int reserved, str contextstring)

#### <a name="parameters"></a>パラメーター

reserved  

<!-- -->

contextstring  

### <a name="method-setxdsbinding"></a>メソッド setXDSBinding

    public void setXDSBinding(str name, str value)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

値  

### <a name="method-setxdsstate"></a>メソッド setXDSState

    public void setXDSState(int finalState)

#### <a name="parameters"></a>パラメーター

finalState  

### <a name="method-setxdstoflushperservicesession"></a>メソッド setXDSToFlushPerServiceSession

サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュされるかどうかを決定する設定を設定します。

    public void setXDSToFlushPerServiceSession(int reserved, int newstate)

#### <a name="parameters"></a>パラメーター

reserved  
サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュするかどうかを示す値。 テーブルにフラッシュする場合は 1 を、フラッシュしない場合は 0 を渡します。

<!-- -->

newstate  
サービス セッションがプールに返されたときに MyConstruct テーブルがフラッシュするかどうかを示す値。 テーブルにフラッシュする場合は 1 を、フラッシュしない場合は 0 を渡します。

### <a name="method-setxdstrace"></a>メソッド setXDSTrace

    public void setXDSTrace(int flag, str value)

#### <a name="parameters"></a>パラメーター

flag  

<!-- -->

値  

## <a name="class-xdynamicvarset"></a>クラス xDynamicVarSet
    class xDynamicVarSet extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法            | 説明 |
|-------------------|-------------|
| public void new() |             |

### <a name="method-new"></a>メソッド new

    public void new()

## <a name="class-xexporttoexcelcontroller"></a>クラス xExportToExcelController
    class xExportToExcelController extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                             | 説明 |
|------------------------------------------------------------------------------------------------------------------------------------|-------------|
| public boolean export()                                                                                                            |             |
| public boolean exportGrid(FormGridControl gridControl, boolean onlyMarkedRows)                                                     |             |
| public boolean performStaticExport(xFormRun formRun, FormGridControl gridControl, System.IO.Stream stream, boolean onlyMarkedRows) |             |
| public void new()                                                                                                                  |             |

### <a name="method-export"></a>メソッド export

    public boolean export()

#### <a name="return-value"></a>戻り値

### <a name="method-exportgrid"></a>メソッド exportGrid

    public boolean exportGrid(FormGridControl gridControl, boolean onlyMarkedRows)

#### <a name="parameters"></a>パラメーター

gridControl  

<!-- -->

onlyMarkedRows  

#### <a name="return-value"></a>戻り値

### <a name="method-performstaticexport"></a>メソッド performStaticExport

    public boolean performStaticExport(xFormRun formRun, FormGridControl gridControl, System.IO.Stream stream, boolean onlyMarkedRows)

#### <a name="parameters"></a>パラメーター

formRun  

<!-- -->

gridControl  

<!-- -->

stream  

<!-- -->

onlyMarkedRows  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new()

## <a name="class-xformrun"></a>クラス xFormRun
    class xFormRun extends ObjectRun

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                                                                                                                                                                         | 説明 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| public boolean allowPrimaryKeyPreview(\[boolean display\])                                                                                                                                                                                                                                                                                                     |             |
| public boolean canClose()                                                                                                                                                                                                                                                                                                                                      |             |
| public boolean canSubmitToWorkflow()                                                                                                                                                                                                                                                                                                                           |             |
| public boolean checkViewOption(int viewOption)                                                                                                                                                                                                                                                                                                                 |             |
| public boolean closed()                                                                                                                                                                                                                                                                                                                                        |             |
| public boolean closedCancel()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean closedOk()                                                                                                                                                                                                                                                                                                                                      |             |
| public boolean contains(FormControl control)                                                                                                                                                                                                                                                                                                                   |             |
| public FormControl control(int controlId)                                                                                                                                                                                                                                                                                                                      |             |
| public FormControl controlCallingMethod()                                                                                                                                                                                                                                                                                                                      |             |
| public int controlId(str controlName)                                                                                                                                                                                                                                                                                                                          |             |
| public boolean controlMethodOverload(\[boolean value\])                                                                                                                                                                                                                                                                                                        |             |
| public Object controlMethodOverloadObject(\[Object value\])                                                                                                                                                                                                                                                                                                    |             |
| public boolean copy()                                                                                                                                                                                                                                                                                                                                          |             |
| public boolean cut()                                                                                                                                                                                                                                                                                                                                           |             |
| public FormObjectSet dataSource(\[AnyType objectSet\])                                                                                                                                                                                                                                                                                                         |             |
| public int dataSourceCount()                                                                                                                                                                                                                                                                                                                                   |             |
| public FormObjectSet defaultDataSource(\[FormObjectSet value\])                                                                                                                                                                                                                                                                                                |             |
| public boolean defaultInitialQueryValuesOnCreate(\[boolean value\])                                                                                                                                                                                                                                                                                            |             |
| public FormDesign design(\[int reserved\])                                                                                                                                                                                                                                                                                                                     |             |
| public Common docCursor()                                                                                                                                                                                                                                                                                                                                      |             |
| public boolean enableCountryRegion(\[boolean flag\])                                                                                                                                                                                                                                                                                                           |             |
| public Form form()                                                                                                                                                                                                                                                                                                                                             |             |
| public Common getActiveWorkflowConfiguration()                                                                                                                                                                                                                                                                                                                 |             |
| public Common getActiveWorkflowTrackingStatus()                                                                                                                                                                                                                                                                                                                |             |
| public Common getActiveWorkflowWorkItem()                                                                                                                                                                                                                                                                                                                      |             |
| public container getAutoCompleteString(int startIdx, \[FormControl control\], \[str searchString\])                                                                                                                                                                                                                                                            |             |
| public str getFormHelpTopic()                                                                                                                                                                                                                                                                                                                                  |             |
| public FormControl getNextField(FormControl control, \[int flags\])                                                                                                                                                                                                                                                                                            |             |
| public FormControl getPrevField(FormControl control, \[int flags\])                                                                                                                                                                                                                                                                                            |             |
| public boolean hasExecutedInit()                                                                                                                                                                                                                                                                                                                               |             |
| public int hWnd()                                                                                                                                                                                                                                                                                                                                              |             |
| public int installMessageProc(int message, int handle, str method)                                                                                                                                                                                                                                                                                             |             |
| public boolean inViewMode()                                                                                                                                                                                                                                                                                                                                    |             |
| public boolean isDataInteractionSupported()                                                                                                                                                                                                                                                                                                                    |             |
| public boolean isPreloadedInstance()                                                                                                                                                                                                                                                                                                                           |             |
| public boolean isFormPart()                                                                                                                                                                                                                                                                                                                                    |             |
| public boolean isFactBox()                                                                                                                                                                                                                                                                                                                                     |             |
| public boolean isLookupForm()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean isPartRemote()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean isPartLocal()                                                                                                                                                                                                                                                                                                                                   |             |
| public boolean isWorkflowEnabled()                                                                                                                                                                                                                                                                                                                             |             |
| public Common loadWorkflowConfiguration()                                                                                                                                                                                                                                                                                                                      |             |
| public boolean lockWindowUpdate(boolean lock)                                                                                                                                                                                                                                                                                                                  |             |
| public str name()                                                                                                                                                                                                                                                                                                                                              |             |
| public FormObjectSet objectSet(\[AnyType objectSet\])                                                                                                                                                                                                                                                                                                          |             |
| public boolean resetAsyncOperationsPendingState()                                                                                                                                                                                                                                                                                                              |             |
| public PageInteraction pageInteraction()                                                                                                                                                                                                                                                                                                                       |             |
| public boolean paste()                                                                                                                                                                                                                                                                                                                                         |             |
| public str recordingScopeId()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean removeMessageProc(int message, int handle)                                                                                                                                                                                                                                                                                                      |             |
| public List rootFormDataSources()                                                                                                                                                                                                                                                                                                                              |             |
| public boolean selectControl(FormControl control)                                                                                                                                                                                                                                                                                                              |             |
| public FormControl selectedControl()                                                                                                                                                                                                                                                                                                                           |             |
| public Common selectRecordModeSelectedRecord(\[Common selectedRecord\])                                                                                                                                                                                                                                                                                        |             |
| public FormControl selectTarget(\[FormControl target\])                                                                                                                                                                                                                                                                                                        |             |
| public Array tabOrder(\[Array newValue\])                                                                                                                                                                                                                                                                                                                      |             |
| public int task(int taskId)                                                                                                                                                                                                                                                                                                                                    |             |
| public str toString()                                                                                                                                                                                                                                                                                                                                          |             |
| public FormObjectSet workflowDataSource()                                                                                                                                                                                                                                                                                                                      |             |
| public str workflowType()                                                                                                                                                                                                                                                                                                                                      |             |
| public System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[str callbackFormMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\]) |             |
| public System.Threading.Tasks.Task setTimeoutEx(\[str formMethodName\], \[container parms\], \[int delay\], \[System.Threading.CancellationToken cancellationToken\])                                                                                                                                                                                          |             |
| public void setParentHandle(int hwnd)                                                                                                                                                                                                                                                                                                                          |             |
| public void setFormHelpTopic(str formHelpTopic)                                                                                                                                                                                                                                                                                                                |             |
| public void setFactBoxEditable()                                                                                                                                                                                                                                                                                                                               |             |
| public void setAutoCompleteString(str string, AnyType control)                                                                                                                                                                                                                                                                                                 |             |
| public void RaiseOnClosing(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                                |             |
| public void inlineLoadingKey(FormControl parentControl)                                                                                                                                                                                                                                                                                                        |             |
| public void closeSelect(str selectString)                                                                                                                                                                                                                                                                                                                      |             |
| public void RaiseOnActivated(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                              |             |
| public void prevField(\[int flags\])                                                                                                                                                                                                                                                                                                                           |             |
| public void send()                                                                                                                                                                                                                                                                                                                                             |             |
| public void RaiseOnInitializing(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                           |             |
| public void updateWorkflowControls()                                                                                                                                                                                                                                                                                                                           |             |
| public void closeCancel()                                                                                                                                                                                                                                                                                                                                      |             |
| public void lastField(\[int flags\])                                                                                                                                                                                                                                                                                                                           |             |
| public void wait(\[boolean modal\])                                                                                                                                                                                                                                                                                                                            |             |
| public void unLock(\[boolean arrangeNow\])                                                                                                                                                                                                                                                                                                                     |             |
| private void OnInitialized(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                           |             |
| public void detach()                                                                                                                                                                                                                                                                                                                                           |             |
| public void resetStatusBarBackgroundColor()                                                                                                                                                                                                                                                                                                                    |             |
| private void OnClosing(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                               |             |
| public void addDisplayMethod(str name, int displayKind, int displayType, int displayXType, int displayRecord, \[str dataSourceName\], \[boolean isTableDisplayMethod\])                                                                                                                                                                                        |             |
| public void print()                                                                                                                                                                                                                                                                                                                                            |             |
| public void activate(boolean active)                                                                                                                                                                                                                                                                                                                           |             |
| public void resize(int width, int height)                                                                                                                                                                                                                                                                                                                      |             |
| public void reload(\[xArgs args\])                                                                                                                                                                                                                                                                                                                             |             |
| public void finalize()                                                                                                                                                                                                                                                                                                                                         |             |
| public void RaiseOnInitialized(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                            |             |
| public void resetSize()                                                                                                                                                                                                                                                                                                                                        |             |
| public void clientId(str clientId)                                                                                                                                                                                                                                                                                                                             |             |
| public void createRecord(str formDataSourceName, \[boolean append\])                                                                                                                                                                                                                                                                                           |             |
| public void firstField(\[int flags\])                                                                                                                                                                                                                                                                                                                          |             |
| public void savePersonalization(str controlName, str propertyKey, str propertyValue)                                                                                                                                                                                                                                                                           |             |
| public void expandFactBoxPaneAtStart()                                                                                                                                                                                                                                                                                                                         |             |
| public void redraw()                                                                                                                                                                                                                                                                                                                                           |             |
| public void arrange()                                                                                                                                                                                                                                                                                                                                          |             |
| public void blockPersonalization(boolean blockPersonalization)                                                                                                                                                                                                                                                                                                 |             |
| public void nextField(\[int flags\])                                                                                                                                                                                                                                                                                                                           |             |
| public void nextGroup()                                                                                                                                                                                                                                                                                                                                        |             |
| public void prevGroup()                                                                                                                                                                                                                                                                                                                                        |             |
| public void setFormPartStyle(boolean isFactBox)                                                                                                                                                                                                                                                                                                                |             |
| public void run()                                                                                                                                                                                                                                                                                                                                              |             |
| public void setActive()                                                                                                                                                                                                                                                                                                                                        |             |
| public void closeSelectRecord(Common selectedRecord)                                                                                                                                                                                                                                                                                                           |             |
| public void registerFormSpecializedCustomControl(str customControlName)                                                                                                                                                                                                                                                                                        |             |
| public void setApply(Object object, \[Object parm\])                                                                                                                                                                                                                                                                                                           |             |
| public void new(xArgs args)                                                                                                                                                                                                                                                                                                                                    |             |
| public void RegisterXppILImplementation(str className)                                                                                                                                                                                                                                                                                                         |             |
| public void sysColorChanged()                                                                                                                                                                                                                                                                                                                                  |             |
| public void selectRecordMode(\[FormControl control\])                                                                                                                                                                                                                                                                                                          |             |
| private void OnPostRun(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                               |             |
| public void skipSaveUserSetting(boolean skip)                                                                                                                                                                                                                                                                                                                  |             |
| public void selectMode(\[FormControl control\])                                                                                                                                                                                                                                                                                                                |             |
| public void printPreview()                                                                                                                                                                                                                                                                                                                                     |             |
| private void OnActivated(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                             |             |
| public void collapseFactBoxPaneAtStart()                                                                                                                                                                                                                                                                                                                       |             |
| public void lock()                                                                                                                                                                                                                                                                                                                                             |             |
| public void init()                                                                                                                                                                                                                                                                                                                                             |             |
| public void formOnTop()                                                                                                                                                                                                                                                                                                                                        |             |
| public void close()                                                                                                                                                                                                                                                                                                                                            |             |
| public void delAutoCompleteString(\[AnyType control\])                                                                                                                                                                                                                                                                                                         |             |
| public void closeOk()                                                                                                                                                                                                                                                                                                                                          |             |
| public void modeledQueryName(str queryName)                                                                                                                                                                                                                                                                                                                    |             |
| public void initWorkflowControls()                                                                                                                                                                                                                                                                                                                             |             |
| public void setOrder(FormControl control, FormControl control1, \[boolean before\])                                                                                                                                                                                                                                                                            |             |
| public void allowCrossFormLinks(boolean allowCrossFormLinks)                                                                                                                                                                                                                                                                                                   |             |
| public void RaiseOnPostRun(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                                |             |
| public void setStatusBarBackgroundColor(int a, int r, int g, int b)                                                                                                                                                                                                                                                                                            |             |
| public void loadPersonalization()                                                                                                                                                                                                                                                                                                                              |             |
| public void doApply()                                                                                                                                                                                                                                                                                                                                          |             |
| private void OnInitializing(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                          |             |
| public void flushCountryRegionCodeCache()                                                                                                                                                                                                                                                                                                                      |             |
| public void localRefresh()                                                                                                                                                                                                                                                                                                                                     |             |

### <a name="method-allowprimarykeypreview"></a>メソッド allowPrimaryKeyPreview

    public boolean allowPrimaryKeyPreview([boolean display])

#### <a name="parameters"></a>パラメーター

表示  

#### <a name="return-value"></a>戻り値

### <a name="method-canclose"></a>メソッド canClose

    public boolean canClose()

#### <a name="return-value"></a>戻り値

### <a name="method-cansubmittoworkflow"></a>メソッド canSubmitToWorkflow

    public boolean canSubmitToWorkflow()

#### <a name="return-value"></a>戻り値

### <a name="method-checkviewoption"></a>メソッド checkViewOption

    public boolean checkViewOption(int viewOption)

#### <a name="parameters"></a>パラメーター

viewOption  

#### <a name="return-value"></a>戻り値

### <a name="method-closed"></a>メソッド closed

    public boolean closed()

#### <a name="return-value"></a>戻り値

### <a name="method-closedcancel"></a>メソッド closedCancel

    public boolean closedCancel()

#### <a name="return-value"></a>戻り値

### <a name="method-closedok"></a>メソッド closedOk

    public boolean closedOk()

#### <a name="return-value"></a>戻り値

### <a name="method-contains"></a>メソッド contains

    public boolean contains(FormControl control)

#### <a name="parameters"></a>パラメーター

control  

#### <a name="return-value"></a>戻り値

### <a name="method-control"></a>メソッド control

    public FormControl control(int controlId)

#### <a name="parameters"></a>パラメーター

controlId  

#### <a name="return-value"></a>戻り値

### <a name="method-controlcallingmethod"></a>メソッド controlCallingMethod

    public FormControl controlCallingMethod()

#### <a name="return-value"></a>戻り値

### <a name="method-controlid"></a>メソッド controlId

    public int controlId(str controlName)

#### <a name="parameters"></a>パラメーター

controlName  

#### <a name="return-value"></a>戻り値

### <a name="method-controlmethodoverload"></a>メソッド controlMethodOverload

    public boolean controlMethodOverload([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-controlmethodoverloadobject"></a>メソッド controlMethodOverloadObject

    public Object controlMethodOverloadObject([Object value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-copy"></a>メソッド copy

    public boolean copy()

#### <a name="return-value"></a>戻り値

### <a name="method-cut"></a>メソッド cut

    public boolean cut()

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

    public FormObjectSet dataSource([AnyType objectSet])

#### <a name="parameters"></a>パラメーター

objectSet  

#### <a name="return-value"></a>戻り値

### <a name="method-datasourcecount"></a>メソッド dataSourceCount

    public int dataSourceCount()

#### <a name="return-value"></a>戻り値

### <a name="method-defaultdatasource"></a>メソッド defaultDataSource

    public FormObjectSet defaultDataSource([FormObjectSet value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-defaultinitialqueryvaluesoncreate"></a>メソッド defaultInitialQueryValuesOnCreate

    public boolean defaultInitialQueryValuesOnCreate([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-design"></a>メソッド design

    public FormDesign design([int reserved])

#### <a name="parameters"></a>パラメーター

reserved  

#### <a name="return-value"></a>戻り値

### <a name="method-doccursor"></a>メソッド docCursor

    public Common docCursor()

#### <a name="return-value"></a>戻り値

### <a name="method-enablecountryregion"></a>メソッド enableCountryRegion

    public boolean enableCountryRegion([boolean flag])

#### <a name="parameters"></a>パラメーター

flag  

#### <a name="return-value"></a>戻り値

### <a name="method-form"></a>メソッド form

    public Form form()

#### <a name="return-value"></a>戻り値

### <a name="method-getactiveworkflowconfiguration"></a>メソッド getActiveWorkflowConfiguration

    public Common getActiveWorkflowConfiguration()

#### <a name="return-value"></a>戻り値

### <a name="method-getactiveworkflowtrackingstatus"></a>メソッド getActiveWorkflowTrackingStatus

    public Common getActiveWorkflowTrackingStatus()

#### <a name="return-value"></a>戻り値

### <a name="method-getactiveworkflowworkitem"></a>メソッド getActiveWorkflowWorkItem

    public Common getActiveWorkflowWorkItem()

#### <a name="return-value"></a>戻り値

### <a name="method-getautocompletestring"></a>メソッド getAutoCompleteString

    public container getAutoCompleteString(int startIdx, [FormControl control], [str searchString])

#### <a name="parameters"></a>パラメーター

startIdx  

<!-- -->

control  

<!-- -->

searchString  

#### <a name="return-value"></a>戻り値

### <a name="method-getformhelptopic"></a>メソッド getFormHelpTopic

    public str getFormHelpTopic()

#### <a name="return-value"></a>戻り値

### <a name="method-getnextfield"></a>メソッド getNextField

    public FormControl getNextField(FormControl control, [int flags])

#### <a name="parameters"></a>パラメーター

control  

<!-- -->

flags  

#### <a name="return-value"></a>戻り値

### <a name="method-getprevfield"></a>メソッド getPrevField

    public FormControl getPrevField(FormControl control, [int flags])

#### <a name="parameters"></a>パラメーター

control  

<!-- -->

flags  

#### <a name="return-value"></a>戻り値

### <a name="method-hasexecutedinit"></a>メソッド hasExecutedInit

    public boolean hasExecutedInit()

#### <a name="return-value"></a>戻り値

### <a name="method-hwnd"></a>メソッド hWnd

    public int hWnd()

#### <a name="return-value"></a>戻り値

### <a name="method-installmessageproc"></a>メソッド installMessageProc

    public int installMessageProc(int message, int handle, str method)

#### <a name="parameters"></a>パラメーター

メッセージ  

<!-- -->

handle  

<!-- -->

メソッド  

#### <a name="return-value"></a>戻り値

### <a name="method-inviewmode"></a>メソッド inViewMode

    public boolean inViewMode()

#### <a name="return-value"></a>戻り値

### <a name="method-isdatainteractionsupported"></a>メソッド isDataInteractionSupported

    public boolean isDataInteractionSupported()

#### <a name="return-value"></a>戻り値

### <a name="method-ispreloadedinstance"></a>メソッド isPreloadedInstance

    public boolean isPreloadedInstance()

#### <a name="return-value"></a>戻り値

### <a name="method-isformpart"></a>メソッド isFormPart

    public boolean isFormPart()

#### <a name="return-value"></a>戻り値

### <a name="method-isfactbox"></a>メソッド isFactBox

    public boolean isFactBox()

#### <a name="return-value"></a>戻り値

### <a name="method-islookupform"></a>メソッド isLookupForm

    public boolean isLookupForm()

#### <a name="return-value"></a>戻り値

### <a name="method-ispartremote"></a>メソッド isPartRemote

    public boolean isPartRemote()

#### <a name="return-value"></a>戻り値

### <a name="method-ispartlocal"></a>メソッド isPartLocal

    public boolean isPartLocal()

#### <a name="return-value"></a>戻り値

### <a name="method-isworkflowenabled"></a>メソッド isWorkflowEnabled

    public boolean isWorkflowEnabled()

#### <a name="return-value"></a>戻り値

### <a name="method-loadworkflowconfiguration"></a>メソッド loadWorkflowConfiguration

    public Common loadWorkflowConfiguration()

#### <a name="return-value"></a>戻り値

### <a name="method-lockwindowupdate"></a>メソッド lockWindowUpdate

    public boolean lockWindowUpdate(boolean lock)

#### <a name="parameters"></a>パラメーター

lock  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-objectset"></a>メソッド objectSet

    public FormObjectSet objectSet([AnyType objectSet])

#### <a name="parameters"></a>パラメーター

objectSet  

#### <a name="return-value"></a>戻り値

### <a name="method-resetasyncoperationspendingstate"></a>メソッド resetAsyncOperationsPendingState

    public boolean resetAsyncOperationsPendingState()

#### <a name="return-value"></a>戻り値

### <a name="method-pageinteraction"></a>メソッド pageInteraction

    public PageInteraction pageInteraction()

#### <a name="return-value"></a>戻り値

### <a name="method-paste"></a>メソッド paste

    public boolean paste()

#### <a name="return-value"></a>戻り値

### <a name="method-recordingscopeid"></a>メソッド recordingScopeId

    public str recordingScopeId()

#### <a name="return-value"></a>戻り値

### <a name="method-removemessageproc"></a>メソッド removeMessageProc

    public boolean removeMessageProc(int message, int handle)

#### <a name="parameters"></a>パラメーター

メッセージ  

<!-- -->

handle  

#### <a name="return-value"></a>戻り値

### <a name="method-rootformdatasources"></a>メソッド rootFormDataSources

    public List rootFormDataSources()

#### <a name="return-value"></a>戻り値

### <a name="method-selectcontrol"></a>メソッド selectControl

    public boolean selectControl(FormControl control)

#### <a name="parameters"></a>パラメーター

control  

#### <a name="return-value"></a>戻り値

### <a name="method-selectedcontrol"></a>メソッド selectedControl

    public FormControl selectedControl()

#### <a name="return-value"></a>戻り値

### <a name="method-selectrecordmodeselectedrecord"></a>メソッド selectRecordModeSelectedRecord

    public Common selectRecordModeSelectedRecord([Common selectedRecord])

#### <a name="parameters"></a>パラメーター

selectedRecord  

#### <a name="return-value"></a>戻り値

### <a name="method-selecttarget"></a>メソッド selectTarget

    public FormControl selectTarget([FormControl target])

#### <a name="parameters"></a>パラメーター

target  

#### <a name="return-value"></a>戻り値

### <a name="method-taborder"></a>メソッド tabOrder

    public Array tabOrder([Array newValue])

#### <a name="parameters"></a>パラメーター

newValue  

#### <a name="return-value"></a>戻り値

### <a name="method-task"></a>メソッド task

    public int task(int taskId)

#### <a name="parameters"></a>パラメーター

taskId  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

    public str toString()

#### <a name="return-value"></a>戻り値

### <a name="method-workflowdatasource"></a>メソッド workflowDataSource

    public FormObjectSet workflowDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-workflowtype"></a>メソッド workflowType

    public str workflowType()

#### <a name="return-value"></a>戻り値

### <a name="method-runasync"></a>メソッド runAsync

    public System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, [System.Threading.CancellationToken cancellationToken], [str callbackFormMethodName], [container asyncState], [str userId], [str company], [str language], [str partitionKey], [System.Threading.Tasks.TaskCreationOptions options])

#### <a name="parameters"></a>パラメーター

runAsClassId  

<!-- -->

runAsStaticMethodName  

<!-- -->

parms  

<!-- -->

cancellationToken  

<!-- -->

callbackFormMethodName  

<!-- -->

asyncState  

<!-- -->

userId  

<!-- -->

会社  

<!-- -->

言語  

<!-- -->

partitionKey  

<!-- -->

オプション  

#### <a name="return-value"></a>戻り値

### <a name="method-settimeoutex"></a>メソッド setTimeoutEx

    public System.Threading.Tasks.Task setTimeoutEx([str formMethodName], [container parms], [int delay], [System.Threading.CancellationToken cancellationToken])

#### <a name="parameters"></a>パラメーター

formMethodName  

<!-- -->

parms  

<!-- -->

遅延  

<!-- -->

cancellationToken  

#### <a name="return-value"></a>戻り値

### <a name="method-setparenthandle"></a>メソッド setParentHandle

    public void setParentHandle(int hwnd)

#### <a name="parameters"></a>パラメーター

hwnd  

### <a name="method-setformhelptopic"></a>メソッド setFormHelpTopic

    public void setFormHelpTopic(str formHelpTopic)

#### <a name="parameters"></a>パラメーター

formHelpTopic  

### <a name="method-setfactboxeditable"></a>メソッド setFactBoxEditable

    public void setFactBoxEditable()

### <a name="method-setautocompletestring"></a>メソッド setAutoCompleteString

    public void setAutoCompleteString(str string, AnyType control)

#### <a name="parameters"></a>パラメーター

string  

<!-- -->

control  

### <a name="method-raiseonclosing"></a>メソッド RaiseOnClosing

    public void RaiseOnClosing([FormEventArgs e])

#### <a name="parameters"></a>パラメーター

e  

### <a name="method-inlineloadingkey"></a>メソッド inlineLoadingKey

    public void inlineLoadingKey(FormControl parentControl)

#### <a name="parameters"></a>パラメーター

parentControl  

### <a name="method-closeselect"></a>メソッド closeSelect

    public void closeSelect(str selectString)

#### <a name="parameters"></a>パラメーター

selectString  

### <a name="method-raiseonactivated"></a>メソッド RaiseOnActivated

    public void RaiseOnActivated([FormEventArgs e])

#### <a name="parameters"></a>パラメーター

e  

### <a name="method-prevfield"></a>メソッド prevField

    public void prevField([int flags])

#### <a name="parameters"></a>パラメーター

flags  

### <a name="method-send"></a>メソッド send

    public void send()

### <a name="method-raiseoninitializing"></a>メソッド RaiseOnInitializing

    public void RaiseOnInitializing([FormEventArgs e])

#### <a name="parameters"></a>パラメーター

e  

### <a name="method-updateworkflowcontrols"></a>メソッド updateWorkflowControls

    public void updateWorkflowControls()

### <a name="method-closecancel"></a>メソッド closeCancel

    public void closeCancel()

### <a name="method-lastfield"></a>メソッド lastField

    public void lastField([int flags])

#### <a name="parameters"></a>パラメーター

flags  

### <a name="method-wait"></a>メソッド wait

    public void wait([boolean modal])

#### <a name="parameters"></a>パラメーター

modal  

### <a name="method-unlock"></a>メソッド unLock

    public void unLock([boolean arrangeNow])

#### <a name="parameters"></a>パラメーター

arrangeNow  

### <a name="method-oninitialized"></a>メソッド OnInitialized

    private void OnInitialized([xFormRun sender], [FormEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-detach"></a>メソッド detach

    public void detach()

### <a name="method-resetstatusbarbackgroundcolor"></a>メソッド resetStatusBarBackgroundColor

    public void resetStatusBarBackgroundColor()

### <a name="method-onclosing"></a>メソッド OnClosing

    private void OnClosing([xFormRun sender], [FormEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-adddisplaymethod"></a>メソッド addDisplayMethod

    public void addDisplayMethod(str name, int displayKind, int displayType, int displayXType, int displayRecord, [str dataSourceName], [boolean isTableDisplayMethod])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

displayKind  

<!-- -->

displayType  

<!-- -->

displayXType  

<!-- -->

displayRecord  

<!-- -->

dataSourceName  

<!-- -->

isTableDisplayMethod  

### <a name="method-print"></a>メソッド print

    public void print()

### <a name="method-activate"></a>メソッド activate

    public void activate(boolean active)

#### <a name="parameters"></a>パラメーター

有効  

### <a name="method-resize"></a>メソッド resize

    public void resize(int width, int height)

#### <a name="parameters"></a>パラメーター

width  

<!-- -->

height  

### <a name="method-reload"></a>メソッド reload

    public void reload([xArgs args])

#### <a name="parameters"></a>パラメーター

args  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-raiseoninitialized"></a>メソッド RaiseOnInitialized

    public void RaiseOnInitialized([FormEventArgs e])

#### <a name="parameters"></a>パラメーター

e  

### <a name="method-resetsize"></a>メソッド resetSize

    public void resetSize()

### <a name="method-clientid"></a>メソッド clientId

    public void clientId(str clientId)

#### <a name="parameters"></a>パラメーター

clientId  

### <a name="method-createrecord"></a>メソッド createRecord

    public void createRecord(str formDataSourceName, [boolean append])

#### <a name="parameters"></a>パラメーター

formDataSourceName  

<!-- -->

append  

### <a name="method-firstfield"></a>メソッド firstField

    public void firstField([int flags])

#### <a name="parameters"></a>パラメーター

flags  

### <a name="method-savepersonalization"></a>メソッド savePersonalization

    public void savePersonalization(str controlName, str propertyKey, str propertyValue)

#### <a name="parameters"></a>パラメーター

controlName  

<!-- -->

propertyKey  

<!-- -->

propertyValue  

### <a name="method-expandfactboxpaneatstart"></a>メソッド expandFactBoxPaneAtStart

    public void expandFactBoxPaneAtStart()

### <a name="method-redraw"></a>メソッド redraw

    public void redraw()

### <a name="method-arrange"></a>メソッド arrange

    public void arrange()

### <a name="method-blockpersonalization"></a>メソッド blockPersonalization

    public void blockPersonalization(boolean blockPersonalization)

#### <a name="parameters"></a>パラメーター

blockPersonalization  

### <a name="method-nextfield"></a>メソッド nextField

    public void nextField([int flags])

#### <a name="parameters"></a>パラメーター

flags  

### <a name="method-nextgroup"></a>メソッド nextGroup

    public void nextGroup()

### <a name="method-prevgroup"></a>メソッド prevGroup

    public void prevGroup()

### <a name="method-setformpartstyle"></a>メソッド setFormPartStyle

    public void setFormPartStyle(boolean isFactBox)

#### <a name="parameters"></a>パラメーター

isFactBox  

### <a name="method-run"></a>メソッド run

    public void run()

### <a name="method-setactive"></a>メソッド setActive

    public void setActive()

### <a name="method-closeselectrecord"></a>メソッド closeSelectRecord

    public void closeSelectRecord(Common selectedRecord)

#### <a name="parameters"></a>パラメーター

selectedRecord  

### <a name="method-registerformspecializedcustomcontrol"></a>メソッド registerFormSpecializedCustomControl

    public void registerFormSpecializedCustomControl(str customControlName)

#### <a name="parameters"></a>パラメーター

customControlName  

### <a name="method-setapply"></a>メソッド setApply

    public void setApply(Object object, [Object parm])

#### <a name="parameters"></a>パラメーター

オブジェクト  

<!-- -->

parm  

### <a name="method-new"></a>メソッド new

    public void new(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

### <a name="method-registerxppilimplementation"></a>メソッド RegisterXppILImplementation

    public void RegisterXppILImplementation(str className)

#### <a name="parameters"></a>パラメーター

className  

### <a name="method-syscolorchanged"></a>メソッド sysColorChanged

    public void sysColorChanged()

### <a name="method-selectrecordmode"></a>メソッド selectRecordMode

    public void selectRecordMode([FormControl control])

#### <a name="parameters"></a>パラメーター

control  

### <a name="method-onpostrun"></a>メソッド OnPostRun

    private void OnPostRun([xFormRun sender], [FormEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-skipsaveusersetting"></a>メソッド skipSaveUserSetting

    public void skipSaveUserSetting(boolean skip)

#### <a name="parameters"></a>パラメーター

skip  

### <a name="method-selectmode"></a>メソッド selectMode

    public void selectMode([FormControl control])

#### <a name="parameters"></a>パラメーター

control  

### <a name="method-printpreview"></a>メソッド printPreview

    public void printPreview()

### <a name="method-onactivated"></a>メソッド OnActivated

    private void OnActivated([xFormRun sender], [FormEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-collapsefactboxpaneatstart"></a>メソッド collapseFactBoxPaneAtStart

    public void collapseFactBoxPaneAtStart()

### <a name="method-lock"></a>メソッド lock

    public void lock()

### <a name="method-init"></a>メソッド init

    public void init()

### <a name="method-formontop"></a>メソッド formOnTop

    public void formOnTop()

### <a name="method-close"></a>メソッド close

    public void close()

### <a name="method-delautocompletestring"></a>メソッド delAutoCompleteString

    public void delAutoCompleteString([AnyType control])

#### <a name="parameters"></a>パラメーター

control  

### <a name="method-closeok"></a>メソッド closeOk

    public void closeOk()

### <a name="method-modeledqueryname"></a>メソッド modeledQueryName

    public void modeledQueryName(str queryName)

#### <a name="parameters"></a>パラメーター

queryName  

### <a name="method-initworkflowcontrols"></a>メソッド initWorkflowControls

    public void initWorkflowControls()

### <a name="method-setorder"></a>メソッド setOrder

    public void setOrder(FormControl control, FormControl control1, [boolean before])

#### <a name="parameters"></a>パラメーター

control  

<!-- -->

control1  

<!-- -->

以前  

### <a name="method-allowcrossformlinks"></a>メソッド allowCrossFormLinks

    public void allowCrossFormLinks(boolean allowCrossFormLinks)

#### <a name="parameters"></a>パラメーター

allowCrossFormLinks  

### <a name="method-raiseonpostrun"></a>メソッド RaiseOnPostRun

    public void RaiseOnPostRun([FormEventArgs e])

#### <a name="parameters"></a>パラメーター

e  

### <a name="method-setstatusbarbackgroundcolor"></a>メソッド setStatusBarBackgroundColor

    public void setStatusBarBackgroundColor(int a, int r, int g, int b)

#### <a name="parameters"></a>パラメーター

a  

<!-- -->

r  

<!-- -->

g  

<!-- -->

b  

### <a name="method-loadpersonalization"></a>メソッド loadPersonalization

    public void loadPersonalization()

### <a name="method-doapply"></a>メソッド doApply

    public void doApply()

### <a name="method-oninitializing"></a>メソッド OnInitializing

    private void OnInitializing([xFormRun sender], [FormEventArgs e])

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

e  

### <a name="method-flushcountryregioncodecache"></a>メソッド flushCountryRegionCodeCache

    public void flushCountryRegionCodeCache()

### <a name="method-localrefresh"></a>メソッド localRefresh

    public void localRefresh()

## <a name="class-xglobal"></a>クラス xGlobal
    class xGlobal extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                                                                                                                                                                                                                                                                                                                                                                             | 説明                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| ::public static ClientType clientKind()                                                                                                                                                                                                                                                                                                                                                            |                                                    |
| ::public static SelectableDataArea company(TableId tableid, \[SelectableDataArea company\])                                                                                                                                                                                                                                                                                                        |                                                    |
| ::public static str computerName()                                                                                                                                                                                                                                                                                                                                                                 |                                                    |
| ::public static boolean hasClient()                                                                                                                                                                                                                                                                                                                                                                |                                                    |
| ::public static int infologLine()                                                                                                                                                                                                                                                                                                                                                                  | 情報ログ バッファの明細行の数を返します。 |
| ::public static boolean isAOS()                                                                                                                                                                                                                                                                                                                                                                    |                                                    |
| ::public static boolean isGuest()                                                                                                                                                                                                                                                                                                                                                                  |                                                    |
| ::public static boolean isUserLanguageRTL()                                                                                                                                                                                                                                                                                                                                                        |                                                    |
| ::public static container languageList()                                                                                                                                                                                                                                                                                                                                                           |                                                    |
| ::public static str machineTzDisplayName()                                                                                                                                                                                                                                                                                                                                                         |                                                    |
| ::public static boolean isObjectOnServer(AnyType object)                                                                                                                                                                                                                                                                                                                                           |                                                    |
| ::public static int randomPositiveInt32()                                                                                                                                                                                                                                                                                                                                                          |                                                    |
| ::public static boolean terminalServer()                                                                                                                                                                                                                                                                                                                                                           |                                                    |
| ::public static WorkerSessionType workerSessionType()                                                                                                                                                                                                                                                                                                                                              |                                                    |
| ::public static System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[int callbackClassId\], \[str callbackStaticMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\]) |                                                    |
| ::public static System.Threading.Tasks.Task runAsyncWithObjectCallback(int runAsClassId, str runAsStaticMethodName, container parms, Object callbackObject, str callbackStaticMethodName)                                                                                                                                                                                                          |                                                    |
| ::public static void forceFormPreload()                                                                                                                                                                                                                                                                                                                                                            | フォームのプリロードが直ちに発生するよう強制します。       |
| private void new()                                                                                                                                                                                                                                                                                                                                                                                 | xGlobal クラスの新しいインスタンスを初期化します。   |

### <a name="method-clientkind"></a>メソッド clientKind

    public static ClientType clientKind()

#### <a name="return-value"></a>戻り値

### <a name="method-company"></a>メソッド company

    public static SelectableDataArea company(TableId tableid, [SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

tableid  

<!-- -->

会社  

#### <a name="return-value"></a>戻り値

### <a name="method-computername"></a>メソッド computerName

    public static str computerName()

#### <a name="return-value"></a>戻り値

### <a name="method-hasclient"></a>メソッド hasClient

    public static boolean hasClient()

#### <a name="return-value"></a>戻り値

### <a name="method-infologline"></a>メソッド infologLine

情報ログ バッファの明細行の数を返します。

    public static int infologLine()

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

このメソッドは、xInfo.line メソッドと同様の機能を持ちますが、サーバーサイド コードを実行しているときにパフォーマンスが向上し、ネットワークの負荷が軽減されます。 XInfo.line は、サーバーで実行されると、クライアントを呼び出して、情報ログ バッファ内の行数を取得します。 xGlobal::infologLine メソッドは、サーバー側の Infolog バッファの行数を取得するので、クライアントに呼び出す必要はありません。 xGlobal::infologLine メソッドは、クライアント上で呼び出されると、クライアント上の情報ログ バッファから行数を直接返します。 このメソッドは、例外を処理するサーバー側のコードを記述するときに特に便利です。 情報ログの行数は、通常、try/catch ブロックが入力される前に保存されます。 例外が発生すると、以前に保存した明細行の数は、try ブロック内のコード中にログ記録されたメッセージを決定するために使用されます。 例外が発生しない場合、保存されている情報ログ バッファ ライン数が多くの場合に使用されます。 xInfo.line メソッドの代わりに xGlobal::infologLine メソッドを使用して情報ログ行を取得することで、クライアントへのラウンド トリップを回避できます。

### <a name="method-isaos"></a>メソッド isAOS

    public static boolean isAOS()

#### <a name="return-value"></a>戻り値

### <a name="method-isguest"></a>メソッド isGuest

    public static boolean isGuest()

#### <a name="return-value"></a>戻り値

### <a name="method-isuserlanguagertl"></a>メソッド isUserLanguageRTL

    public static boolean isUserLanguageRTL()

#### <a name="return-value"></a>戻り値

### <a name="method-languagelist"></a>メソッド languageList

    public static container languageList()

#### <a name="return-value"></a>戻り値

### <a name="method-machinetzdisplayname"></a>メソッド machineTzDisplayName

    public static str machineTzDisplayName()

#### <a name="return-value"></a>戻り値

### <a name="method-isobjectonserver"></a>メソッド isObjectOnServer

    public static boolean isObjectOnServer(AnyType object)

#### <a name="parameters"></a>パラメーター

オブジェクト  

#### <a name="return-value"></a>戻り値

### <a name="method-randompositiveint32"></a>メソッド randomPositiveInt32

    public static int randomPositiveInt32()

#### <a name="return-value"></a>戻り値

### <a name="method-terminalserver"></a>メソッド terminalServer

    public static boolean terminalServer()

#### <a name="return-value"></a>戻り値

### <a name="method-workersessiontype"></a>メソッド workerSessionType

    public static WorkerSessionType workerSessionType()

#### <a name="return-value"></a>戻り値

### <a name="method-runasync"></a>メソッド runAsync

    public static System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, [System.Threading.CancellationToken cancellationToken], [int callbackClassId], [str callbackStaticMethodName], [container asyncState], [str userId], [str company], [str language], [str partitionKey], [System.Threading.Tasks.TaskCreationOptions options])

#### <a name="parameters"></a>パラメーター

runAsClassId  

<!-- -->

runAsStaticMethodName  

<!-- -->

parms  

<!-- -->

cancellationToken  

<!-- -->

callbackClassId  

<!-- -->

callbackStaticMethodName  

<!-- -->

asyncState  

<!-- -->

userId  

<!-- -->

会社  

<!-- -->

言語  

<!-- -->

partitionKey  

<!-- -->

オプション  

#### <a name="return-value"></a>戻り値

### <a name="method-runasyncwithobjectcallback"></a>メソッド runAsyncWithObjectCallback

    public static System.Threading.Tasks.Task runAsyncWithObjectCallback(int runAsClassId, str runAsStaticMethodName, container parms, Object callbackObject, str callbackStaticMethodName)

#### <a name="parameters"></a>パラメーター

runAsClassId  

<!-- -->

runAsStaticMethodName  

<!-- -->

parms  

<!-- -->

callbackObject  

<!-- -->

callbackStaticMethodName  

#### <a name="return-value"></a>戻り値

### <a name="method-forceformpreload"></a>メソッド forceFormPreload

フォームのプリロードが直ちに発生するよう強制します。

    public static void forceFormPreload()

#### <a name="remarks"></a>備考

通常、クライアントがアイドルになったときのみ、プリロードが発生します。 実行時間の長い X++ の実行が発生しているシナリオでは、このメソッドを強制的にフォームのプリロードを行うために使用できます。

### <a name="method-new"></a>メソッド new

xGlobal クラスの新しいインスタンスを初期化します。

    private void new()

## <a name="class-xinfo"></a>クラス xInfo
    class xInfo extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                       | 説明                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int removeMessage(Int64 messageId)                                                                                                                                                                    |                                                                                                                                                                                         |
| public Int64 insertMessage(MessageSeverity type, str message)                                                                                                                                                |                                                                                                                                                                                         |
| public Exception add(Exception exceptionType, str string, \[str helpURL\], \[Object obj\], \[boolean buildprefix\])                                                                                          | 情報ログ バッファに文字列を追加します。                                                                                                                                                    |
| public Exception addException(str string, str stackTrace)                                                                                                                                                    |                                                                                                                                                                                         |
| public container breakpoint(\[container breakpoint\])                                                                                                                                                        | ブレークポイントに関する情報を取得または設定します。                                                                                                                                             |
| public boolean canShowCreateRuleMenuItem(xFormRun caller)                                                                                                                                                    | フォームの警告ルール作成フォームのメニュー項目を表示するかどうかを決定します。                                                                                         |
| public boolean canShutdown(boolean silent)                                                                                                                                                                   | システムをシャットダウンできるかどうかをテストします。 このメソッドを使用しないでください。 代わりに、Info クラスでオーバーライドされたバージョンを使用します。                                                        |
| public boolean canViewAlertInbox()                                                                                                                                                                           | 現在のユーザーに警告の表示フォームを表示するアクセス許可があるかどうかを判断します。                                                                                                        |
| public xCompilerOutput compilerOutput(\[Object compilerOut\])                                                                                                                                                | コンパイラ出力オブジェクトを取得または設定します。 コンパイラ出力オブジェクトは、デフォルトでコンパイラ出力ウィンドウです。                                                                           |
| public container copy(int from, int to)                                                                                                                                                                      | 情報ログ バッファーから行をコピーします。                                                                                                                                                   |
| public int createDevelopmentWorkspaceWindow()                                                                                                                                                                |                                                                                                                                                                                         |
| public int createWorkspaceWindow()                                                                                                                                                                           | 新しいワークスペース ウィンドウを開きます。 たとえば、これにより、異なるウィンドウでアプリケーション オブジェクトの異なるセットを開く、または会社コードの 2 つの異なるセットを使用することができます。 |
| public UtilEntryLevel currentAOLayer()                                                                                                                                                                       | SYS または USR などで実行している現在の階層を取得します。                                                                                                                     |
| public container cut(int from, int to)                                                                                                                                                                       | 情報ログ バッファーから行を切り取りします。                                                                                                                                                     |
| public str documentationLanguage(\[str languageCode\])                                                                                                                                                       | Finance and Operations のドキュメントに使用される言語を取得または設定します。                                                                                                     |
| public container export()                                                                                                                                                                                    |                                                                                                                                                                                         |
| public TreeNode findNode(str nodePath)                                                                                                                                                                       | 指定されたツリー ノードを取得します。                                                                                                                                                    |
| public TreeNode getDocNode(UtilFileType helpType, int UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel UtilLevel\], \[boolean ForceLevel\], \[int Mode\], \[boolean OldUtil\]) | AOT から指定したドキュメント ノードを取得します。                                                                                                                               |
| public TreeNode getImportedNode(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)                                                                                    | XPO ファイルからツリー ノードのインスタンスを作成しますが、AOT にインポートしません。 たとえば、これにより、同じツリー ノードの別のバージョンと比較できます。         |
| public TreeNode getNode(UtilElementType UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[int Mode\], \[boolean OldUtil\])               | AOT 内のノードに対応するツリー ノードを取得します。                                                                                                                            |
| public int getNodeResid(UtilElementType nodeType)                                                                                                                                                            | 指定したタイプのノードを表示するために使用されるアイコンのリソース ID を取得します。                                                                                             |
| public Struct getTaskInfo(int taskNumber)                                                                                                                                                                    |                                                                                                                                                                                         |
| public UserSetup getUserSetup()                                                                                                                                                                              | ユーザー パラメーターを設定するために使用する UserSetup オブジェクトを取得します。                                                                                                                       |
| public container getWorkspaceList()                                                                                                                                                                          |                                                                                                                                                                                         |
| public int hWnd(\[int workspaceNum\])                                                                                                                                                                        | Finance and OperationsNavigation ウィンドウのハンドルを取得します。                                                                                                                  |
| public boolean import(container infologContainer, \[boolean clearExistingInfolog\])                                                                                                                          |                                                                                                                                                                                         |
| public int importElement(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)                                                                                           | インポートする対象を指定します。                                                                                                                                                    |
| public int importString(str source, UtilElementType kind, str name)                                                                                                                                          | ファイルからオブジェクトをインポートします。                                                                                                                                                          |
| public int instance()                                                                                                                                                                                        | アプリケーションの現在のインスタンスへのハンドルを取得します。                                                                                                                          |
| public str isoCurrencyCode(\[str code\])                                                                                                                                                                     | 通貨コードを取得または設定します。                                                                                                                                                         |
| public boolean IsVisible()                                                                                                                                                                                   | クライアントのウィンドウが最小化されていないかどうかを決定します。                                                                                                                                  |
| public str language(\[str languageCode\])                                                                                                                                                                    | GUI の言語を取得または設定します。                                                                                                                                                  |
| public Exception level(int line)                                                                                                                                                                             | 情報ログ バッファー内の行の例外レベルを取得します。                                                                                                                          |
| public int line()                                                                                                                                                                                            | 情報ログ バッファの明細行の数を取得します。                                                                                                                                    |
| public MessageWin messageWin()                                                                                                                                                                               | Infolog から Message ウィンドウに出力を送信できます。                                                                                                                      |
| public Real nationalCurrencyFactor(\[Real factor\])                                                                                                                                                          |                                                                                                                                                                                         |
| public str nationalCurrencyPostfix(\[str string\])                                                                                                                                                           |                                                                                                                                                                                         |
| public str nationalCurrencyPrefix(\[str string\])                                                                                                                                                            |                                                                                                                                                                                         |
| public xNavPane navPane()                                                                                                                                                                                    | プライマリ ナビゲーション コントロール クラスの xNavPane オブジェクトを取得します。                                                                                                                     |
| public int num(\[Exception exceptionType\])                                                                                                                                                                  | 情報ログ バッファにおける指定した型の例外の数を取得します。                                                                                                         |
| public int prevInstance()                                                                                                                                                                                    | アプリケーションの前のインスタンスへのハンドルを取得します。                                                                                                                         |
| public int processId()                                                                                                                                                                                       | Finance and Operations プロセスの ID を取得します。                                                                                                                                 |
| public TreeNode projectRootNode()                                                                                                                                                                            | X++ プロジェクト ノードを返します。                                                                                                                                                          |
| public TreeNode rootNode()                                                                                                                                                                                   | アプリケーション オブジェクト ツリーのルートを取得します。                                                                                                                                      |
| public int startImport(str file, int flag, \[str labelSubstitutes\])                                                                                                                                         | インポート コンテキストを作成します。                                                                                                                                                              |
| public str text(\[int line\])                                                                                                                                                                                | 情報ログからテキストの行を取得します。                                                                                                                                              |
| public TreeNode userNode()                                                                                                                                                                                   |                                                                                                                                                                                         |
| public AnyType webSession(\[AnyType value\])                                                                                                                                                                 |                                                                                                                                                                                         |
| ::public static container activeXControls()                                                                                                                                                                  | Finance and Operations にある ActiveX コントロールの一覧を取得します。                                                                                                             |
| ::public static str AOTLogDirectory()                                                                                                                                                                        | 現在のインストールのログ ディレクトリへのパスを取得します。                                                                                                                        |
| ::public static container automationObjects()                                                                                                                                                                | Finance and Operations で使用可能な COM オブジェクトの一覧を取得します。                                                                                                          |
| ::public static str buildNo()                                                                                                                                                                                | 現在の Finance and Operations 実行可能ファイルのカーネル ビルド番号を取得します。                                                                                                      |
| ::public static str compilationDate()                                                                                                                                                                        | Finance and Operations の現在のバージョンが最後にコンパイルされた日付を取得します。                                                                                             |
| ::public static str compilationTime()                                                                                                                                                                        | Finance and Operations の現在のバージョンが最後にコンパイルされた時刻を取得します。                                                                                             |
| ::public static str componentName()                                                                                                                                                                          | コンポーネントへのパスを取得します。                                                                                                                                                    |
| ::public static str configuration()                                                                                                                                                                          | 現在のクライアント構成を取得します。                                                                                                                                             |
| ::public static int currentWorkspaceNum()                                                                                                                                                                    | 現在のワークスペースのアプリケーション ウィンドウ ID を取得します。                                                                                                                           |
| ::public static str directory(DirectoryType type)                                                                                                                                                            | Finance and Operations クライアントがインストールされているディレクトリへのパスを取得します。                                                                                          |
| ::public static Date expireDate()                                                                                                                                                                            | 現在のインストールのライセンスの有効期限が切れる日付を取得します。                                                                                                           |
| ::public static ApplicationObjectTreeWindow getApplicationObjectTreeWindow()                                                                                                                                 |                                                                                                                                                                                         |
| ::public static int getCurrentModelId()                                                                                                                                                                      |                                                                                                                                                                                         |
| ::public static int getNumberOfDecimals(Real number)                                                                                                                                                         | 指定された数値の小数点以下の桁数を取得します。                                                                                                                         |
| ::public static PropertiesWindow getPropertiesWindow()                                                                                                                                                       |                                                                                                                                                                                         |
| ::public static int getSystemGeneratedModelId(UtilEntryLevel layer)                                                                                                                                          |                                                                                                                                                                                         |
| ::public static str licenseName()                                                                                                                                                                            | 現在の Finance and Operations ライセンスの名前を取得します。                                                                                                                        |
| ::public static str productName()                                                                                                                                                                            | 製品の名前を取得します。                                                                                                                                                      |
| ::public static str productRegisteredName()                                                                                                                                                                  |                                                                                                                                                                                         |
| ::public static str releaseVersion()                                                                                                                                                                         | 現在の Finance and Operations 実行可能ファイルのバージョン番号 (3.0 や 4.0 など) を取得します。                                                                                 |
| ::public static str releaseYear()                                                                                                                                                                            |                                                                                                                                                                                         |
| ::public static str serialNo()                                                                                                                                                                               | 現在の Finance and Operations ライセンスのシリアル番号を取得します。                                                                                                               |
| public void new()                                                                                                                                                                                            | 新しい xInfo オブジェクトを初期化します。                                                                                                                                                         |
| public void workspaceWindowDestroyed(int hWnd)                                                                                                                                                               | 新しいワークスペースが終了した時に実行します。                                                                                                                                                    |
| public void writeCustomStatlineItem(str text)                                                                                                                                                                | テキストの行をステータス バーに記述します。                                                                                                                                                |
| public void reloadRunningMode()                                                                                                                                                                              |                                                                                                                                                                                         |
| public void setWindowOrder(int window, \[int afterWindow\])                                                                                                                                                  | Windows の表示順序を設定します。                                                                                                                                    |
| public void shutDown(boolean force)                                                                                                                                                                          | クライアントをシャットダウンします。                                                                                                                                                                  |
| public void xref(str path, xRef x)                                                                                                                                                                           | 相互参照システムが使用される時に実行します。                                                                                                                                       |
| public void updateCurrentCompany()                                                                                                                                                                           |                                                                                                                                                                                         |
| public void redrawAllWindows()                                                                                                                                                                               | すべてのウィンドウを再描画します。                                                                                                                                                                    |
| public void formNotify(xFormRun form, FormNotify notification, \[FormNotifyEventArgs formNotifyEventArgs\])                                                                                                  | 特定フォームへの変更特定タイプに基づいて実行し、カスタムコードの実行を許可します。                                                                                          |
| public void mayReloadMenu(boolean value)                                                                                                                                                                     | UI を更新できないようにする                                                                                                                                                        |
| public void startLengthyOperation()                                                                                                                                                                          | マウス カーソルをアイドルに設定します。                                                                                                                                                          |
| public void breakpointNotify(BreakpointNotify notification)                                                                                                                                                  | ブレークポイントが変更されたときの通知システムを実装します。                                                                                                                          |
| public void initializeInfolog(int window)                                                                                                                                                                    |                                                                                                                                                                                         |
| public void startup(str startupCmd)                                                                                                                                                                          | クライアントの起動時に実行します。                                                                                                                                                        |
| public void endImport(int id, int elements)                                                                                                                                                                  | インポート プロセスを完了します。                                                                                                                                                            |
| public void yield()                                                                                                                                                                                          |                                                                                                                                                                                         |
| public void viewAlertInbox(\[int selectedTab\])                                                                                                                                                              | 警告の表示フォームを起動します。                                                                                                                                                          |
| public void reportSendMailServer(PrintJobSettings settings)                                                                                                                                                  |                                                                                                                                                                                         |
| public void endLengthyOperation(\[boolean endAll\])                                                                                                                                                          | startLengthyOperation の呼び出し後にマウス カーソルが標準に戻るように設定します。                                                                                                             |
| public void setNumUnreadAlerts(\[int n\])                                                                                                                                                                    | 未読の警告メールの数が変わると、ステータス バーのテキストを更新します。                                                                                                          |
| public void truncate(str prefix)                                                                                                                                                                             | 情報ログから指定した接頭語の付いた品目を削除します。                                                                                                                           |
| public void formNoteButton(boolean enable, boolean value)                                                                                                                                                    | ツールバーのドキュメント処理ボタンをコントロールします。                                                                                                                                   |
| public void viewCreateRuleDialog(xFormRun caller)                                                                                                                                                            | 警告ルールの作成フォームを起動します。                                                                                                                                                    |
| public void view(\[container container\])                                                                                                                                                                    |                                                                                                                                                                                         |
| public void clear(\[int linesLeft\])                                                                                                                                                                         | 情報ログ バッファーから行を削除します。                                                                                                                                                  |
| public void workspaceWindowCreated(int hWnd)                                                                                                                                                                 | 新しいワークスペースが作成された時に実行します。                                                                                                                                               |
| ::public static void setCurrentModelId(int currentModelId)                                                                                                                                                   |                                                                                                                                                                                         |
| public void activateMenubarTask(int command)                                                                                                                                                                 |                                                                                                                                                                                         |
| public void finalize()                                                                                                                                                                                       |                                                                                                                                                                                         |
| public void insertXReferences()                                                                                                                                                                              |                                                                                                                                                                                         |
| public void activateButton(int command)                                                                                                                                                                      |                                                                                                                                                                                         |
| public void activateWindow(int window)                                                                                                                                                                       | フォームまたはウィンドウにフォーカスを設定します。                                                                                                                                                     |
| public void reportSendMail(PrintJobSettings settings)                                                                                                                                                        | レポートを電子メールで送信するための設定を生成します。                                                                                                                                   |

### <a name="method-removemessage"></a>メソッド removeMessage

    public int removeMessage(Int64 messageId)

#### <a name="parameters"></a>パラメーター

messageId  

#### <a name="return-value"></a>戻り値

### <a name="method-insertmessage"></a>メソッド insertMessage

    public Int64 insertMessage(MessageSeverity type, str message)

#### <a name="parameters"></a>パラメーター

タイプ  

<!-- -->

メッセージ  

#### <a name="return-value"></a>戻り値

### <a name="method-add"></a>メソッド add

情報ログ バッファに文字列を追加します。

    public Exception add(Exception exceptionType, str string, [str helpURL], [Object obj], [boolean buildprefix])

#### <a name="parameters"></a>パラメーター

exceptionType  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

string  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

helpURL  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

obj  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

<!-- -->

buildprefix  
オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。

#### <a name="return-value"></a>戻り値

例外システム列挙値です。 詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。

#### <a name="remarks"></a>備考

helpURL パラメーターの値の例は、「KernDoc:\\\\\\\\ 機能 \\\\substr」です。 このメソッドは直接使用しないでください。 代わりに、infolog.info、infolog.warning、infolog.error、または infolog.checkFailed メソッドを使用します。 ExceptionType パラメーターの詳細については、トライおよびキャッチ キーワードで例外処理を参照してください。

### <a name="method-addexception"></a>メソッド addException

    public Exception addException(str string, str stackTrace)

#### <a name="parameters"></a>パラメーター

string  

<!-- -->

stackTrace  

#### <a name="return-value"></a>戻り値

### <a name="method-breakpoint"></a>メソッド breakpoint

ブレークポイントに関する情報を取得または設定します。

    public container breakpoint([container breakpoint])

#### <a name="parameters"></a>パラメーター

ブレークポイント  
現在のブレークポイントに関する情報を保持するコンテナーです。

#### <a name="return-value"></a>戻り値

現在のブレークポイントに関する情報を保持するコンテナーです。

#### <a name="remarks"></a>備考

ブレークポイントに関する情報を保持するコンテナーの形式は次のとおりです。

-   項目 1: バージョン番号
-   項目 2 - 4、5-7、… n - n+2: 各ブレークポイントに関する以下の情報
    -   AOT パス
    -   ブレークポイントがセットされている行番号
    -   ブレークポイントが有効または無効かどうか

アプリケーションで、このメソッドはブレークポイント フォームで使用されます。 このフォームは、開いているときに、フォームに対して getBreakpoints メソッドを呼び出します。 これは、xInfo.breakpoint メソッドを呼び出し、ブレークポイント情報を持つコンテナーをパラメーターとして使用します。 ブレークポイントを無効にするとき、有効にするとき、またはフォームから削除するとき、setBreakpoints メソッドが呼び出されます。 これにより、ブレークポイントに関する情報が更新され、ブレークポイント パラメーターを使用せずに xInfo.breakpoint メソッドを使用してコンテナーとして返されます。 コンテナーは、コード エディター ウィンドウのブレークポイント情報を更新するために使用されます。

### <a name="method-canshowcreaterulemenuitem"></a>メソッド canShowCreateRuleMenuItem

フォームの警告ルール作成フォームのメニュー項目を表示するかどうかを決定します。

    public boolean canShowCreateRuleMenuItem(xFormRun caller)

#### <a name="parameters"></a>パラメーター

caller  
現在のフォーム: 警告ルールの作成メニュー項目が表示されるフォーム。

#### <a name="return-value"></a>戻り値

現在のフォームが警告の作成をサポートする場合は true。それ以外の場合は false。

### <a name="method-canshutdown"></a>メソッド canShutdown

システムをシャットダウンできるかどうかをテストします。 このメソッドを使用しないでください。 代わりに、Info クラスでオーバーライドされたバージョンを使用します。

    public boolean canShutdown(boolean silent)

#### <a name="parameters"></a>パラメーター

silent  
ユーザーがシステムを終了したいか尋ねるかどうかを決定するブール値。

#### <a name="return-value"></a>戻り値

システムをシャットダウンすることができる場合は true。それ以外の場合は、false。

### <a name="method-canviewalertinbox"></a>メソッド canViewAlertInbox

現在のユーザーに警告の表示フォームを表示するアクセス許可があるかどうかを判断します。

    public boolean canViewAlertInbox()

#### <a name="return-value"></a>戻り値

ユーザーがフォームを表示するためのアクセス許可を持つ場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

xInfo.viewAlertInbox を呼び出す前に、このメソッドを呼び出します。

### <a name="method-compileroutput"></a>メソッド compilerOutput

コンパイラ出力オブジェクトを取得または設定します。 コンパイラ出力オブジェクトは、デフォルトでコンパイラ出力ウィンドウです。

    public xCompilerOutput compilerOutput([Object compilerOut])

#### <a name="parameters"></a>パラメーター

compilerOut  
コンパイラ出力オブジェクト; オプション。 オプションのパラメーター。

#### <a name="return-value"></a>戻り値

xCompilerOutput オブジェクト。

#### <a name="remarks"></a>備考

compilerOut パラメーターの既定値は、コンパイラ出力ウィンドウですが、メッセージ ウィンドウでもあります。

### <a name="method-copy"></a>メソッド copy

情報ログ バッファーから行をコピーします。

    public container copy(int from, int to)

#### <a name="parameters"></a>パラメーター

投稿者  
コピーする最後の行。

<!-- -->

終了  
コピーする最後の行。

#### <a name="return-value"></a>戻り値

開始日と終了の間の情報ログ行を含むコンテナー。

#### <a name="examples"></a>例

次の例では、copy メソッドを使用して、情報ログの内容をログにコピーします。

    boolean validateRecord() 
    { 
        boolean     ok = true; 
        ok = intrastat.validateRecord(); 
        if (ok) 
            intrastat.log = ''; 
        else 
        { 
            intrastat.log = Info::infoCon2Str( 
                infolog.copy(infoLogCounter+1,infolog.num())); 
            infoLogCounter = infolog.num(); 
            errorFound = true; 
        } 
        intrastat.update(); 
        return ok; 
    }

### <a name="method-createdevelopmentworkspacewindow"></a>メソッド createDevelopmentWorkspaceWindow

    public int createDevelopmentWorkspaceWindow()

#### <a name="return-value"></a>戻り値

### <a name="method-createworkspacewindow"></a>メソッド createWorkspaceWindow

新しいワークスペース ウィンドウを開きます。 たとえば、これにより、異なるウィンドウでアプリケーション オブジェクトの異なるセットを開く、または会社コードの 2 つの異なるセットを使用することができます。

    public int createWorkspaceWindow()

#### <a name="return-value"></a>戻り値

新規のウィンドウにハンドルを返します。

### <a name="method-currentaolayer"></a>メソッド currentAOLayer

SYS または USR などで実行している現在の階層を取得します。

    public UtilEntryLevel currentAOLayer()

#### <a name="return-value"></a>戻り値

作業中の現在のレイヤーを示す UtilEntryLevel システム列挙値。

#### <a name="remarks"></a>備考

詳細については、「レイヤー」を参照してください。

### <a name="method-cut"></a>メソッド cut

情報ログ バッファーから行を切り取りします。

    public container cut(int from, int to)

#### <a name="parameters"></a>パラメーター

投稿者  
カットする最後の行。

<!-- -->

終了  
カットする最後の行。

#### <a name="return-value"></a>戻り値

「～から」と「～へ」のパラメーターで指定された行の間の情報ログ行を保持するコンテナーです。

#### <a name="examples"></a>例

次の例では、fromLine 値で指定された行から最後の行まで Infolog の行を切り取ります。

    private void cutInfolog(int fromLine) 
    { 
        infolog.cut(fromLine+1, Global::infologLine()); 
    }

### <a name="method-documentationlanguage"></a>メソッド documentationLanguage

Finance and Operations のドキュメントに使用される言語を取得または設定します。

    public str documentationLanguage([str languageCode])

#### <a name="parameters"></a>パラメーター

languageCode  
設定する言語の ID。オプション。

#### <a name="return-value"></a>戻り値

ドキュメントに現在使用されている言語の ID。

#### <a name="remarks"></a>備考

GUI の言語を設定するには、xInfo.language メソッドを使用します。 特定のセッションのドキュメント言語を設定するには、xSession.documentationLanguage メソッドを使用します。 languageCode パラメーターの値の例は「en-us」で、英語 (US) の言語に設定されます。

### <a name="method-export"></a>メソッド export

    public container export()

#### <a name="return-value"></a>戻り値

### <a name="method-findnode"></a>メソッド findNode

指定されたツリー ノードを取得します。

    public TreeNode findNode(str nodePath)

#### <a name="parameters"></a>パラメーター

nodePath  
ノードへのパスを含む文字列。

#### <a name="return-value"></a>戻り値

nodePath パラメーターで指定されるツリー ノードを返します。

#### <a name="remarks"></a>備考

 メソッドは廃止されています。 代わりに TreeNode::findNode メソッドを使用してください。

### <a name="method-getdocnode"></a>メソッド getDocNode

AOT から指定したドキュメント ノードを取得します。

    public TreeNode getDocNode(UtilFileType helpType, int UtilType, str Name, [UtilElementId ParentId], [int Type], [UtilEntryLevel UtilLevel], [boolean ForceLevel], [int Mode], [boolean OldUtil])

#### <a name="parameters"></a>パラメーター

helpType  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

UtilType  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

氏名  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

ParentId  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

種類  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

UtilLevel  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

ForceLevel  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

モード  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

OldUtil  
oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

AOT からのドキュメント ノードです。

#### <a name="remarks"></a>備考

helpType パラメーターの使用可能な値は、UtilFileType システム列挙の値です。

-   KernelHelp: システム ドキュメント ノード
-   ApplicationHelp: アプリケーション ドキュメント ノード
-   ApplicationCodeDocumentation: アプリケーション開発者ドキュメント ノード。

utilType パラメーターの値の例は、システム ドキュメント ノード内の機能ノードです。 ForceLevel パラメーターの既定値は false です。 False に設定され、指定されたレイヤーでコンテンツがない場合は、ノードはコンテンツを持つ次のレイヤーから取得されます。 true に設定され、レイヤーにコンテンツがない場合、メソッドは nullNothingnullptrunita null 参照 (Visual Basic 上ではなし) を返します。

### <a name="method-getimportednode"></a>メソッド getImportedNode

XPO ファイルからツリー ノードのインスタンスを作成しますが、AOT にインポートしません。 たとえば、これにより、同じツリー ノードの別のバージョンと比較できます。

    public TreeNode getImportedNode(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)

#### <a name="parameters"></a>パラメーター

id  

<!-- -->

utilfiletype  

<!-- -->

utiltype  

<!-- -->

名前  

<!-- -->

fileposition  

<!-- -->

フラグ  

#### <a name="return-value"></a>戻り値

ツリー ノード。

#### <a name="remarks"></a>備考

tilfiletype パラメーターの使用可能な値は UtilFileType 列挙で使用可能な値です。 utiltype パラメーターの使用可能な値は UtilElementType 列挙で使用可能な値です。 フラグ パラメーターの可能な値の一覧については、AOTExport マクロを参照してください。 値は、システム インポート フラグ コメントの下に一覧で表示されています。

#### <a name="examples"></a>例

次の例では、getImportedNode メソッドを使用して仮想ツリー ノードを作成します。

    public TreeNode getVirtualTreenode( 
        Filename _filename = this.fileName()) 
    { 
        #AOT 
        #AotExport 
        TmpAotImport      tmpImportAot; 
        SysImportElements sysImportElements = new SysImportElements(); 
        TreeNode treeNodeImport  = null; 
        int      exportId; 
        int      flag = (#impGetCompareNode + #impKeepIds); 
        str      name; 
        ; 
        // Set the filename. 
        sysImportElements.newFile(_filename); 
        // Get info from the file 
        tmpImportAot = sysImportElements.getTmpImportAot(); 
        // Create an import context 
        exportId     = infolog.startImport(_filename, flag); 
        // Get the right name 
        // for doc nodes it is the path excl. the first part 
        switch (tmpImportAot.UtilFileType) 
        { 
            case UtilFileType::Application: 
                name = tmpImportAot.TreeNodeName; 
                break; 
            case UtilFileType::ApplicationCodeDocumentation: 
                name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#ApplicationDeveloperDocPath)); 
                break; 
            case UtilFileType::ApplicationHelp: 
                name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#ApplicationDocPath)); 
                break; 
            case UtilFileType::KernelHelp: 
                name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#SystemDocPath)); 
                break; 
            default: 
                name = tmpImportAot.TreeNodeName; 
                break; 
        } 
        // Import the node in memory 
        treeNodeImport  = infolog.getImportedNode( 
            exportId, 
            tmpImportAot.UtilFileType, 
            tmpImportAot.UtilElementType, 
            name, 
            tmpImportAot.FilePos, 
            flag); 
        // Close the import context 
        infolog.endImport(exportId, 1); 
        return treeNodeImport; 
    }

### <a name="method-getnode"></a>メソッド getNode

AOT 内のノードに対応するツリー ノードを取得します。

    public TreeNode getNode(UtilElementType UtilType, str Name, [UtilElementId ParentId], [int Type], [UtilEntryLevel Utillevel], [boolean Forcelevel], [int Mode], [boolean OldUtil])

#### <a name="parameters"></a>パラメーター

UtilType  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

氏名  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

ParentId  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

種類  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

Utillevel  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

Forcelevel  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

モード  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

<!-- -->

OldUtil  
古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

UtilType パラメーターおよび Name パラメーターで指定されるツリー ノード。

#### <a name="remarks"></a>備考

戻されたノードは AOT にリンクされていないため、ノードで操作を実行することはできません。 ノードの操作を行うには、代わりに findNode メソッドまたは rootNode メソッドを使用します。 UtilLevel trueparameter パラメーターの既定値は現在のレイヤーです。 Mode パラメーターの使用可能な値は次のとおりです。

-   0x001: 実行用の読み込み
-   0x002: 編集用の読み込み

ForceLevel パラメーターの既定値は false です。 False に設定され、指定されたレイヤーでコンテンツがない場合は、ノードはコンテンツを持つ次のレイヤーから取得されます。 true に設定され、レイヤーにコンテンツがない場合、メソッドは nullNothingnullptrunita null 参照 (Visual Basic 上ではなし) を返します。

### <a name="method-getnoderesid"></a>メソッド getNodeResid

指定したタイプのノードを表示するために使用されるアイコンのリソース ID を取得します。

    public int getNodeResid(UtilElementType nodeType)

#### <a name="parameters"></a>パラメーター

nodeType  
取得するノードのタイプを示す UtilElementType システム列挙値。

#### <a name="return-value"></a>戻り値

ノードのリソース ID を表す整数。

### <a name="method-gettaskinfo"></a>メソッド getTaskInfo

    public Struct getTaskInfo(int taskNumber)

#### <a name="parameters"></a>パラメーター

taskNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-getusersetup"></a>メソッド getUserSetup

ユーザー パラメーターを設定するために使用する UserSetup オブジェクトを取得します。

    public UserSetup getUserSetup()

#### <a name="return-value"></a>戻り値

UserSetup オブジェクト。

#### <a name="remarks"></a>備考

UserSetup システム クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。

### <a name="method-getworkspacelist"></a>メソッド getWorkspaceList

    public container getWorkspaceList()

#### <a name="return-value"></a>戻り値

### <a name="method-hwnd"></a>メソッド hWnd

Finance and OperationsNavigation ウィンドウのハンドルを取得します。

    public int hWnd([int workspaceNum])

#### <a name="parameters"></a>パラメーター

workspaceNum  
ナビゲーション ウィンドウ ハンドルを取得するワークスペースのハンドルです。

#### <a name="return-value"></a>戻り値

Finance and OperationsNavigation ペイン ウィンドウにハンドルを表示する整数。

### <a name="method-import"></a>メソッド import

    public boolean import(container infologContainer, [boolean clearExistingInfolog])

#### <a name="parameters"></a>パラメーター

infologContainer  

<!-- -->

clearExistingInfolog  

#### <a name="return-value"></a>戻り値

### <a name="method-importelement"></a>メソッド importElement

インポートする対象を指定します。

    public int importElement(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)

#### <a name="parameters"></a>パラメーター

id  

<!-- -->

utilfiletype  

<!-- -->

utiltype  

<!-- -->

名前  

<!-- -->

fileposition  

<!-- -->

フラグ  

#### <a name="return-value"></a>戻り値

 メソッドは廃止されています。 代わりに SysImportElements クラスを使用します。

### <a name="method-importstring"></a>メソッド importString

ファイルからオブジェクトをインポートします。

    public int importString(str source, UtilElementType kind, str name)

#### <a name="parameters"></a>パラメーター

ソース  
オブジェクトの名前です。

<!-- -->

kind  
オブジェクトの名前です。

<!-- -->

名前  
オブジェクトの名前です。

#### <a name="return-value"></a>戻り値

### <a name="method-instance"></a>メソッド instance

アプリケーションの現在のインスタンスへのハンドルを取得します。

    public int instance()

#### <a name="return-value"></a>戻り値

アプリケーションの現在のインスタンスのハンドルです。

### <a name="method-isocurrencycode"></a>メソッド isoCurrencyCode

通貨コードを取得または設定します。

    public str isoCurrencyCode([str code])

#### <a name="parameters"></a>パラメーター

コード  
設定する ISO 通貨コードを含む文字列。

#### <a name="return-value"></a>戻り値

現在のアプリケーションの通貨コードを含む文字列。

### <a name="method-isvisible"></a>メソッド IsVisible

クライアントのウィンドウが最小化されていないかどうかを決定します。

    public boolean IsVisible()

#### <a name="return-value"></a>戻り値

クライアント ウィンドウが最小化されている場合は false; それ以外の場合は true。

### <a name="method-language"></a>メソッド language

GUI の言語を取得または設定します。

    public str language([str languageCode])

#### <a name="parameters"></a>パラメーター

languageCode  
設定の言語コードを含む文字列。

#### <a name="return-value"></a>戻り値

現在の言語コードを含む文字列。

#### <a name="remarks"></a>備考

ドキュメントの言語を設定するには、xInfo.documentationLanguage メソッドを使用します。 特定のセッションの GUI 言語を設定するには、xSession.interfaceLanguage メソッドを使用します。

#### <a name="examples"></a>例

次の例では、現在設定されている言語のコードを出力します。 たとえば、インターフェイスが英語 (US) であった場合、「en-us」を印刷します。

    { 
        print infolog.language(); 
        pause; 
    }

### <a name="method-level"></a>メソッド level

情報ログ バッファー内の行の例外レベルを取得します。

    public Exception level(int line)

#### <a name="parameters"></a>パラメーター

明細行  
例外レベルを取得する情報ログの行。

#### <a name="return-value"></a>戻り値

例外システム列挙値。

#### <a name="remarks"></a>備考

詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。

### <a name="method-line"></a>メソッド line

情報ログ バッファの明細行の数を取得します。

    public int line()

#### <a name="return-value"></a>戻り値

情報ログ バッファー内の行数を表す整数。

#### <a name="remarks"></a>備考

サーバーでコードを実行している場合は、代わりに xGlobal::infologLine メソッドを使用します。 サーバーとクライアントの間の呼び出しを除外します。 Infolog 内の特定タイプの例外の数を取得するには、xInfo.num メソッドを使用します。

### <a name="method-messagewin"></a>メソッド messageWin

Infolog から Message ウィンドウに出力を送信できます。

    public MessageWin messageWin()

#### <a name="return-value"></a>戻り値

MessageWin オブジェクト。

#### <a name="remarks"></a>備考

時間がかかるプロセスがある場合は、メッセージ ウィンドウに出力を送信することが必要な場合があります。 情報ログに出力を送信する場合、プロセスが完了するまで何も表示されません。 メッセージ ウィンドウに出力を送信する場合は、工程の進行中のコンテンツが表示されます。

### <a name="method-nationalcurrencyfactor"></a>メソッド nationalCurrencyFactor

    public Real nationalCurrencyFactor([Real factor])

#### <a name="parameters"></a>パラメーター

係数  

#### <a name="return-value"></a>戻り値

### <a name="method-nationalcurrencypostfix"></a>メソッド nationalCurrencyPostfix

    public str nationalCurrencyPostfix([str string])

#### <a name="parameters"></a>パラメーター

string  

#### <a name="return-value"></a>戻り値

### <a name="method-nationalcurrencyprefix"></a>メソッド nationalCurrencyPrefix

    public str nationalCurrencyPrefix([str string])

#### <a name="parameters"></a>パラメーター

string  

#### <a name="return-value"></a>戻り値

### <a name="method-navpane"></a>メソッド navPane

プライマリ ナビゲーション コントロール クラスの xNavPane オブジェクトを取得します。

    public xNavPane navPane()

#### <a name="return-value"></a>戻り値

xNavPane クラスのインスタンス。

#### <a name="remarks"></a>備考

このクラスのインスタンスはワークスペースごとに 1 つのみ持つことができます。

### <a name="method-num"></a>メソッド num

情報ログ バッファにおける指定した型の例外の数を取得します。

    public int num([Exception exceptionType])

#### <a name="parameters"></a>パラメーター

exceptionType  
カウントする例外のタイプを示す例外システム列挙値; オプション。

#### <a name="return-value"></a>戻り値

exceptionType パラメーターで指定されたタイプの例外の数または、パラメーターが指定されていない場合の情報ログ内の行の合計数を表す整数。

#### <a name="remarks"></a>備考

詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。

#### <a name="examples"></a>例

次の例は、Infolog 内の警告の数を返します。

    { 
        print infolog.num(Exception::Warning); 
        pause; 
    }

### <a name="method-previnstance"></a>メソッド prevInstance

アプリケーションの前のインスタンスへのハンドルを取得します。

    public int prevInstance()

#### <a name="return-value"></a>戻り値

アプリケーションの以前のインスタンスのハンドルです。

#### <a name="remarks"></a>備考

このメソッドは使用しないでください。

### <a name="method-processid"></a>メソッド processId

Finance and Operations プロセスの ID を取得します。

    public int processId()

#### <a name="return-value"></a>戻り値

Finance and Operations プロセスの ID。

### <a name="method-projectrootnode"></a>メソッド projectRootNode

X++ プロジェクト ノードを返します。

    public TreeNode projectRootNode()

#### <a name="return-value"></a>戻り値

X++ プロジェクトを含むツリー ノード。

#### <a name="examples"></a>例

次の例では、共有プロジェクト フォルダー内のすべてのプロジェクトの名前を出力します。

    void ProjectNames() 
    { 
        Treenode treenode; 
        TreenodeIterator it; 
        treenode = infolog.projectRootNode(); 
        treenode = treenode.AOTfindChild("Shared"); 
        it = treenode.AOTiterator(); 
        while (treenode) 
        { 
           print treenode.treeNodeName(); 
           treenode = it.next(); 
        } 
        pause; 
    }

### <a name="method-rootnode"></a>メソッド rootNode

アプリケーション オブジェクト ツリーのルートを取得します。

    public TreeNode rootNode()

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクト ツリーのルート。

#### <a name="examples"></a>例

次の例では、AddressSelectForm クラスのメソッドのすべての名前を出力します。 rootnode メソッドは、子ノードを選択する前に、treenode オブジェクトを AOT ルートに設定するために使用されます。

    { 
        Treenode treenode; 
        TreenodeIterator it; 
        treenode = infolog.rootNode(); 
        treenode = treenode.AOTfindChild("Classes"); 
        treenode = treenode.AOTfindChild("AddressSelectForm"); 
        it = treenode.AOTiterator(); 
        while (treenode) 
        { 
           print treenode.treeNodeName(); 
           treenode = it.next(); 
        } 
        pause; 
    }

### <a name="method-startimport"></a>メソッド startImport

インポート コンテキストを作成します。

    public int startImport(str file, int flag, [str labelSubstitutes])

#### <a name="parameters"></a>パラメーター

ファイル  

<!-- -->

flag  

<!-- -->

labelSubstitutes  

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

 メソッドは廃止されています。 代わりに SysImportElements クラスを使用します。

### <a name="method-text"></a>メソッド text

情報ログからテキストの行を取得します。

    public str text([int line])

#### <a name="parameters"></a>パラメーター

明細行  
取得するテキストを含む情報ログ内の行。

#### <a name="return-value"></a>戻り値

情報ログのテキストを含む文字列。

### <a name="method-usernode"></a>メソッド userNode

    public TreeNode userNode()

#### <a name="return-value"></a>戻り値

### <a name="method-websession"></a>メソッド webSession

    public AnyType webSession([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-activexcontrols"></a>メソッド activeXControls

Finance and Operations にある ActiveX コントロールの一覧を取得します。

    public static container activeXControls()

#### <a name="return-value"></a>戻り値

各 ActiveX コントロールに関する情報を保持する入れ子になったコンテナー。

#### <a name="remarks"></a>備考

返されるコンテナーには 4 つのコンテナーがあります。 最初の内部コンテナーには、すべてのコントロールの名前が含まれます。 2 番目の内部コンテナーには、各コントロールの ID (GUID) が格納されます。 3 番目の内部コンテナーには、各コントロールのセキュリティ設定が格納されます。 4 番目の内部コンテナーには、各コントロールの説明が含まれています。

#### <a name="examples"></a>例

次の例では、Finance and Operations の各 ActiveX コントロールの説明を出力します。

    static void activeXcontents(Args _args) 
    { 
        int       i; 
        str       strClsName, strTypeLibHelp, strClsId, strSafeForBits; 
        container c; 
        container clsName, clsId, safeForBits, typeLibHelp; 
        c = xinfo::activeXControls(); 
        clsName = conpeek(c, 1); 
        clsId = conpeek(c, 2); 
        safeForBits = conpeek(c, 3); 
        typeLibHelp = conpeek(c, 4); 
        for (i=1; i<conlen(clsName); i++) 
        { 
            strClsName = conpeek(clsName, i); 
            strClsId = conpeek(clsId, i); 
            strSafeForBits = conpeek(safeForBits, i); 
            strTypeLibHelp = conpeek(typeLibHelp, i); 
            print strClsName, " ", strClsId, " ", strSafeForBits, 
                " ", strTypeLibHelp; 
        } 
        pause; 
    }

### <a name="method-aotlogdirectory"></a>メソッド AOTLogDirectory

現在のインストールのログ ディレクトリへのパスを取得します。

    public static str AOTLogDirectory()

#### <a name="return-value"></a>戻り値

現在のインストールのログ ディレクトリへのパスを含む文字列。

#### <a name="remarks"></a>備考

AOT ログ オプションを有効にする場合は、コンパイルするたびにときに、ログ ディレクトリに情報が保存されます。 このオプションをオンにするには、次のようにします。

1.  開発者ワークスペースを開きます。
2.  [ツール] &gt; [オプション] &gt; [開発]&gt; [コンパイラ] を選択します。
3.  AOT ログ チェック ボックスをオンにします。

### <a name="method-automationobjects"></a>メソッド automationObjects

Finance and Operations で使用可能な COM オブジェクトの一覧を取得します。

    public static container automationObjects()

#### <a name="return-value"></a>戻り値

各 COM オブジェクトの説明を保持する入れ子になったコンテナー。

#### <a name="examples"></a>例

次の例では、automationObject から返される入れ子になったコンテナーを展開して、COM オブジェクトのリストを取得します。

    void getAutomationObjects() 
    { 
        int idx; 
        FormListItem listItem; 
        int itemPos; 
        container clsGUID,clsDesc,clsVersion,clsPath; 
        [clsGUID,clsDesc,clsVersion,clsPath] = xInfo::automationObjects(); 
        for (idx = 1; idx < conlen(clsGUID); idx++) 
        { 
            itemPos = formListControl.add(conpeek(clsDesc,idx)); 
            listItem = formListControl.getItem(itemPos); 
            listItem.data(conpeek(clsPath,idx)); 
            formListControl.setItem(listItem); 
        } 
    }

### <a name="method-buildno"></a>メソッド buildNo

現在の Finance and Operations 実行可能ファイルのカーネル ビルド番号を取得します。

    public static str buildNo()

#### <a name="return-value"></a>戻り値

カーネル ビルド番号を含む文字列。

#### <a name="examples"></a>例

次の例では、このメソッドを使用して、Finance and Operations のバージョン情報を含む文字列の一部としてカーネル ビルド番号を返します。

    static client str axaptaReleaseID() 
    { 
        #define.versionPrefix('v') 
        #define.versionNumber('#') 
        #define.versionPartition('/') 
        return    #versionprefix+xInfo::releaseVersion()+ 
                  #versionNumber+xInfo::buildNo()+ 
                  #versionPartition+ApplicationVersion::buildNo(); 
    }

### <a name="method-compilationdate"></a>メソッド compilationDate

Finance and Operations の現在のバージョンが最後にコンパイルされた日付を取得します。

    public static str compilationDate()

#### <a name="return-value"></a>戻り値

Finance and Operations が最後にコンパイルされた日付を含む文字列。

#### <a name="examples"></a>例

次の例では、アプリケーションが最後にコンパイルされた日付を含むシステム情報を返します。

    str environment() 
    { 
        return xInfo::buildNo() + ' - '  
            + xInfo::compilationDate() + ' - '  
            + xInfo::dbName() + ' - '  
            + xInfo::osName() + ' - '  
            + xInfo::productName() + ' - '  
            + xInfo::releaseVersion(); 
    }

### <a name="method-compilationtime"></a>メソッド compilationTime

Finance and Operations の現在のバージョンが最後にコンパイルされた時刻を取得します。

    public static str compilationTime()

#### <a name="return-value"></a>戻り値

Finance and Operations が最後にコンパイルされた時間を含む文字列。

### <a name="method-componentname"></a>メソッド componentName

コンポーネントへのパスを取得します。

    public static str componentName()

#### <a name="return-value"></a>戻り値

実行可能ファイルへのパスを含む文字列。

#### <a name="remarks"></a>備考

このメソッドがクライアントで実行される場合、Finance and Operations クライアントの .exe ファイルへパスを返します。 サーバーで実行する場合、AOS の .exe ファイルへのパスを返します。

### <a name="method-configuration"></a>メソッド configuration

現在のクライアント構成を取得します。

    public static str configuration()

#### <a name="return-value"></a>戻り値

現在のクライアント コンフィギュレーションを表す文字列。

#### <a name="remarks"></a>備考

これは、クライアント構成ユーティリティー プログラムの「構成」ボックスで選択されている構成です。 返される文字列の例としては「オリジナル (インストール済コンフィギュレーション)」です。

### <a name="method-currentworkspacenum"></a>メソッド currentWorkspaceNum

現在のワークスペースのアプリケーション ウィンドウ ID を取得します。

    public static int currentWorkspaceNum()

#### <a name="return-value"></a>戻り値

現在のワークスペースのアプリケーション ウィンドウ ID。

#### <a name="remarks"></a>備考

createWorkspaceWindow メソッドを使用すると、アプリケーション内で追加のワークスペースを開くことができます。

### <a name="method-directory"></a>メソッド directory

Finance and Operations クライアントがインストールされているディレクトリへのパスを取得します。

    public static str directory(DirectoryType type)

#### <a name="parameters"></a>パラメーター

タイプ  
クライアント インストールのサブフォルダーのいずれかを示す DirectoryType 列挙値。

#### <a name="return-value"></a>戻り値

DirectoryType パラメーターで指定されているディレクトリへのパスを含む文字列。

#### <a name="examples"></a>例

次の例は、現在のクライアント インストールの Bin ディレクトリへのパスを出力します。

    { 
        print xInfo::directory(DirectoryType::Bin); 
        pause; 
    }

### <a name="method-expiredate"></a>メソッド expireDate

現在のインストールのライセンスの有効期限が切れる日付を取得します。

    public static Date expireDate()

#### <a name="return-value"></a>戻り値

ライセンスの有効期限が切れる日を表す日付です。

### <a name="method-getapplicationobjecttreewindow"></a>メソッド getApplicationObjectTreeWindow

    public static ApplicationObjectTreeWindow getApplicationObjectTreeWindow()

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrentmodelid"></a>メソッド getCurrentModelId

    public static int getCurrentModelId()

#### <a name="return-value"></a>戻り値

### <a name="method-getnumberofdecimals"></a>メソッド getNumberOfDecimals

指定された数値の小数点以下の桁数を取得します。

    public static int getNumberOfDecimals(Real number)

#### <a name="parameters"></a>パラメーター

数値  
実数。

#### <a name="return-value"></a>戻り値

数値パラメーターの小数点以下の桁数。

### <a name="method-getpropertieswindow"></a>メソッド getPropertiesWindow

    public static PropertiesWindow getPropertiesWindow()

#### <a name="return-value"></a>戻り値

### <a name="method-getsystemgeneratedmodelid"></a>メソッド getSystemGeneratedModelId

    public static int getSystemGeneratedModelId(UtilEntryLevel layer)

#### <a name="parameters"></a>パラメーター

 レイヤー  

#### <a name="return-value"></a>戻り値

### <a name="method-licensename"></a>メソッド licenseName

現在の Finance and Operations ライセンスの名前を取得します。

    public static str licenseName()

#### <a name="return-value"></a>戻り値

ライセンスの名前を含む文字列。

#### <a name="remarks"></a>備考

xInfo::expireDate メソッドは、ライセンスが失効する日付を返します。 xInfo::serialNo メソッドは、ライセンスのシリアル番号を返します。

### <a name="method-productname"></a>メソッド productName

製品の名前を取得します。

    public static str productName()

#### <a name="return-value"></a>戻り値

製品の名前を含む文字列。

#### <a name="examples"></a>例

次の例では、製品の名前を含むシステム情報を戻します。

    str environment() 
    { 
        return xInfo::buildNo() + ' - '  
            + xInfo::compilationDate() + ' - '  
            + xInfo::dbName() + ' - '  
            + xInfo::osName() + ' - '  
            + xInfo::productName() + ' - '  
            + xInfo::releaseVersion(); 
    }

### <a name="method-productregisteredname"></a>メソッド productRegisteredName

    public static str productRegisteredName()

#### <a name="return-value"></a>戻り値

### <a name="method-releaseversion"></a>メソッド releaseVersion

現在の Finance and Operations 実行可能ファイルのバージョン番号 (3.0 や 4.0 など) を取得します。

    public static str releaseVersion()

#### <a name="return-value"></a>戻り値

Finance and Operations のバージョン番号を含む文字列。

#### <a name="remarks"></a>備考

有効なバージョン番号は、3.0 および 4.0 などです。

#### <a name="examples"></a>例

次の例では、これを使用して、Finance and Operations のバージョン情報を含む文字列の一部としてバージョン番号を返します。

    static client str axaptaReleaseID() 
    { 
        #define.versionPrefix('v') 
        #define.versionNumber('#') 
        #define.versionPartition('/') 
        return    #versionprefix+xInfo::releaseVersion()+ 
                  #versionNumber+xInfo::buildNo()+ 
                  #versionPartition+ApplicationVersion::buildNo(); 
    }

### <a name="method-releaseyear"></a>メソッド releaseYear

    public static str releaseYear()

#### <a name="return-value"></a>戻り値

### <a name="method-serialno"></a>メソッド serialNo

現在の Finance and Operations ライセンスのシリアル番号を取得します。

    public static str serialNo()

#### <a name="return-value"></a>戻り値

Finance and Operations のライセンスのシリアル番号を含む文字列。

### <a name="method-new"></a>メソッド new

新しい xInfo オブジェクトを初期化します。

    public void new()

#### <a name="remarks"></a>備考

注記: このメソッドを使用しないでください。 代わりに、xInfo クラスのグローバル インスタンス infolog を使用する必要があります。 詳細については、「xInfo クラス」を参照してください。

### <a name="method-workspacewindowdestroyed"></a>メソッド workspaceWindowDestroyed

新しいワークスペースが終了した時に実行します。

    public void workspaceWindowDestroyed(int hWnd)

#### <a name="parameters"></a>パラメーター

hWnd  
ワークスペースのハンドルです。

#### <a name="remarks"></a>備考

このメソッドは、新しいワークスペースが閉じられるときに呼び出されます。 これにより、発生したときにアクションを実行できます。

### <a name="method-writecustomstatlineitem"></a>メソッド writeCustomStatlineItem

テキストの行をステータス バーに記述します。

    public void writeCustomStatlineItem(str text)

#### <a name="parameters"></a>パラメーター

テキスト  
ステータス バーに入れるテキストの行。

### <a name="method-reloadrunningmode"></a>メソッド reloadRunningMode

    public void reloadRunningMode()

### <a name="method-setwindoworder"></a>メソッド setWindowOrder

Windows の表示順序を設定します。

    public void setWindowOrder(int window, [int afterWindow])

#### <a name="parameters"></a>パラメーター

window  
ウィンドウ パラメーターで指定されたウィンドウの後に配置するウィンドウのハンドルです (オプション)。

<!-- -->

afterWindow  
ウィンドウ パラメーターで指定されたウィンドウの後に配置するウィンドウのハンドルです (オプション)。

#### <a name="examples"></a>例

次の例では、ウィンドウにフォーカスを設定し、ウィンドウを前面に移動します。

    void setFocus() 
    { 
        infolog.activateWindow(element.hWnd()); 
        infolog.setWindowOrder(element.hWnd()); 
    }

### <a name="method-shutdown"></a>メソッド shutDown

クライアントをシャットダウンします。

    public void shutDown(boolean force)

#### <a name="parameters"></a>パラメーター

force  
シャット ダウンを防止するオプションが、ユーザーに与えられたかどうかを示すブール値。

### <a name="method-xref"></a>メソッド xref

相互参照システムが使用される時に実行します。

    public void xref(str path, xRef x)

#### <a name="parameters"></a>パラメーター

path  

<!-- -->

x  

#### <a name="remarks"></a>備考

このメソッドを使用しないでください。

### <a name="method-updatecurrentcompany"></a>メソッド updateCurrentCompany

    public void updateCurrentCompany()

### <a name="method-redrawallwindows"></a>メソッド redrawAllWindows

すべてのウィンドウを再描画します。

    public void redrawAllWindows()

#### <a name="remarks"></a>備考

このメソッドは、長いプロセス中に表示を更新するために使用できます。

### <a name="method-formnotify"></a>メソッド formNotify

特定フォームへの変更特定タイプに基づいて実行し、カスタムコードの実行を許可します。

    public void formNotify(xFormRun form, FormNotify notification, [FormNotifyEventArgs formNotifyEventArgs])

#### <a name="parameters"></a>パラメーター

フォーム  

<!-- -->

通知  

<!-- -->

formNotifyEventArgs  

#### <a name="remarks"></a>備考

通知パラメーターの使用可能な値は次のとおりです。

-   有効化する
-   DeActivate
-   求人開始
-   終了
-   RecordChange
-   NoteClicked

このメソッドの使用例については、このメソッドが上書きされた情報クラスの formNotify メソッドを参照してください。

### <a name="method-mayreloadmenu"></a>メソッド mayReloadMenu

UI を更新できないようにする

    public void mayReloadMenu(boolean value)

#### <a name="parameters"></a>パラメーター

値  
UI が更新されないようにするかどうかを示すブール値。

#### <a name="remarks"></a>備考

プロセスが実行されたときに UI が更新されないように値を false に設定し、プロセスが終了した後は true に設定します。 mayReloadMenu メソッドは、AOT 内の多くのノードが読み取られているなど、UI がちらつくのを防ぐのに便利です。

### <a name="method-startlengthyoperation"></a>メソッド startLengthyOperation

マウス カーソルをアイドルに設定します。

    public void startLengthyOperation()

#### <a name="remarks"></a>備考

時間のかかる操作の開始時に、プロセスが進行中であることを示すために使用します。 工程が完了したら、システムは endLengthyOperation メソッドを自動的に呼び出します。

### <a name="method-breakpointnotify"></a>メソッド breakpointNotify

ブレークポイントが変更されたときの通知システムを実装します。

    public void breakpointNotify(BreakpointNotify notification)

#### <a name="parameters"></a>パラメーター

通知  
ブレークポイントに発生した変更のタイプを指定する BreakpointNotify システム列挙値。

#### <a name="remarks"></a>備考

アプリケーションで、このメソッドはコード エディター ウィンドウでのブレークポイントの変更時に、ブレークポイント フォームを更新するために使用されます。 通知パラメーターには、次の BreakpointNotify 列挙型の値が有効です。

-   BreakpointForm: ブレークポイント リストを再読み込みする必要があることをクライアントに通知します。
-   BreakpointChange: クライアントとサーバーにブレークポイントの状態が変更 (有効、無効、または削除) されたことを通知します。

### <a name="method-initializeinfolog"></a>メソッド initializeInfolog

    public void initializeInfolog(int window)

#### <a name="parameters"></a>パラメーター

window  

### <a name="method-startup"></a>メソッド startup

クライアントの起動時に実行します。

    public void startup(str startupCmd)

#### <a name="parameters"></a>パラメーター

startupCmd  

#### <a name="remarks"></a>備考

このメソッドを使用しないでください。 代わりに次の方法のいずれかを使用します。 起動コマンドをクライアントに渡すには Info.startupPost メソッドを使用します。 起動コマンドをサーバーに渡すには Application.startupPost メソッドを使用します。 Application.startup または Info.startup メソッドを使用しないでください。 これは、Finance and Operations の新しいバージョンのコードに影響する可能性があり、クライアントまたはサーバーの起動を妨げる可能性があります。

### <a name="method-endimport"></a>メソッド endImport

インポート プロセスを完了します。

    public void endImport(int id, int elements)

#### <a name="parameters"></a>パラメーター

id  

<!-- -->

elements  

#### <a name="remarks"></a>備考

 メソッドは廃止されています。 代わりに SysImportElements クラスを使用します。

### <a name="method-yield"></a>メソッド yield

    public void yield()

### <a name="method-viewalertinbox"></a>メソッド viewAlertInbox

警告の表示フォームを起動します。

    public void viewAlertInbox([int selectedTab])

#### <a name="parameters"></a>パラメーター

selectedTab  
警告の表示フォームが表示されるタブを決定します。オプション。

#### <a name="remarks"></a>備考

selectedTab パラメーターの既定値は、最初のタブである概要です。xInfo.canViewAlertInbox メソッドを呼び出して、ユーザーがこのフォームを表示する権限を持っているかどうかを確認します。

### <a name="method-reportsendmailserver"></a>メソッド reportSendMailServer

    public void reportSendMailServer(PrintJobSettings settings)

#### <a name="parameters"></a>パラメーター

設定  

### <a name="method-endlengthyoperation"></a>メソッド endLengthyOperation

startLengthyOperation の呼び出し後にマウス カーソルが標準に戻るように設定します。

    public void endLengthyOperation([boolean endAll])

#### <a name="parameters"></a>パラメーター

endAll  
予約済み。

#### <a name="remarks"></a>備考

このメソッドを呼び出さないことをお勧めします。 操作が終了すると、システムによって自動的に呼び出されます。 明示的にこのメソッドを呼び出し、その他のプロセスまたはループのコードがある場合は、このメソッドを使用すると、マウス ポインターが点滅する可能性があります。

### <a name="method-setnumunreadalerts"></a>メソッド setNumUnreadAlerts

未読の警告メールの数が変わると、ステータス バーのテキストを更新します。

    public void setNumUnreadAlerts([int n])

#### <a name="parameters"></a>パラメーター

n  
未読メールの数を特定の番号に設定できます。

### <a name="method-truncate"></a>メソッド truncate

情報ログから指定した接頭語の付いた品目を削除します。

    public void truncate(str prefix)

#### <a name="parameters"></a>パラメーター

prefix  
情報ログから削除する必要のある項目の接頭語。

### <a name="method-formnotebutton"></a>メソッド formNoteButton

ツールバーのドキュメント処理ボタンをコントロールします。

    public void formNoteButton(boolean enable, boolean value)

#### <a name="parameters"></a>パラメーター

enable  
アイコンの表示が示すブール値データ型。

<!-- -->

値  
アイコンの表示が示すブール値データ型。

#### <a name="examples"></a>例

次の例は、ドキュメント処理ボタンを無効にする方法を示しています。

    void disableNoteButton() 
        { 
            infolog.formNoteButton(false, false); 
        }

### <a name="method-viewcreateruledialog"></a>メソッド viewCreateRuleDialog

警告ルールの作成フォームを起動します。

    public void viewCreateRuleDialog(xFormRun caller)

#### <a name="parameters"></a>パラメーター

caller  
現在のフォーム。

#### <a name="remarks"></a>備考

作成警告ルール フォームは、呼び出し元のパラメーターで指定された現在のフォームから起動されます。

### <a name="method-view"></a>メソッド view

    public void view([container container])

#### <a name="parameters"></a>パラメーター

コンテナー  

### <a name="method-clear"></a>メソッド clear

情報ログ バッファーから行を削除します。

    public void clear([int linesLeft])

#### <a name="parameters"></a>パラメーター

linesLeft  
バッファに残す行の数、省略可能です。

#### <a name="remarks"></a>備考

他のプロセスが情報を Infolog に入れていない限り、既定値がゼロのメソッドで呼び出さないでください。

#### <a name="examples"></a>例

Infolog キャッシュを消去するには、このパターンを使用します。

    int line = Global::infologLine();
    try 
    { 
        // 
    } 
    catch 
    { 
        infolog.clear(line); 
    }

### <a name="method-workspacewindowcreated"></a>メソッド workspaceWindowCreated

新しいワークスペースが作成された時に実行します。

    public void workspaceWindowCreated(int hWnd)

#### <a name="parameters"></a>パラメーター

hWnd  
新しいワークスペースのハンドルです。

#### <a name="remarks"></a>備考

このメソッドは、新しいワークスペースが作成されるときに呼び出されます。 これにより、発生したときにアクションを実行できます。

### <a name="method-setcurrentmodelid"></a>メソッド setCurrentModelId

    public static void setCurrentModelId(int currentModelId)

#### <a name="parameters"></a>パラメーター

currentModelId  

### <a name="method-activatemenubartask"></a>メソッド activateMenubarTask

    public void activateMenubarTask(int command)

#### <a name="parameters"></a>パラメーター

command  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-insertxreferences"></a>メソッド insertXReferences

    public void insertXReferences()

### <a name="method-activatebutton"></a>メソッド activateButton

    public void activateButton(int command)

#### <a name="parameters"></a>パラメーター

command  

### <a name="method-activatewindow"></a>メソッド activateWindow

フォームまたはウィンドウにフォーカスを設定します。

    public void activateWindow(int window)

#### <a name="parameters"></a>パラメーター

window  
詳しく説明するフォームまたはウィンドウのハンドルです。

### <a name="method-reportsendmail"></a>メソッド reportSendMail

レポートを電子メールで送信するための設定を生成します。

    public void reportSendMail(PrintJobSettings settings)

#### <a name="parameters"></a>パラメーター

設定  
ユーザーの電子メール設定。

## <a name="class-xlanguage"></a>クラス xLanguage
    class xLanguage extends Object

xLanguage クラスは、言語 ID のリストと既存のラベル ファイルに関する情報へのアクセスを提供します。

### <a name="remarks"></a>備考

ISO 639 は、英語の "en" などの言語の名前を定義します。 Microsoft は、英語 (米国) の場合は「en-us」といった一連の言語コードをリストしました。 これらの言語コードは、Finance and Operations で言語 ID として参照されます。 Finance and Operations は、「ko-jo」を使用して韓国語 (Johab) を表します。 Microsoft のリストで、「ko」は韓国語と韓国語 (Johab) の両方です。 Finance and Operations は、「no-ny」を使用してノルウェー語 (ニーノシュク) を表します。 Microsoft のリストで、「no」はノルウェー語 (ブークモール) とノルウェー語 (ニーノシク) の両方です。 Finance and Operations は、「es-tr」を使用してスペイン語 (スペイン - トラディショナル ソート) を表します。 Microsoft のリストで、「es」はスペイン語 (スペイン - モダン ソート) とスペイン語 (スペイン - トラディショナル ソート) の両方です。 「英語 (米国)」など、次の形式での言語名は、Finance and Operations の説明と呼ばれます。

### <a name="examples"></a>例

次の例では、すべての言語 ID を Microsoft のリストと既存のラベル ファイルのリストから出力します。

    static void aaaTestLanguage(args a) 
    { 
        int i; 
        int cnt; 
        str languageID; 
        str description; 
        str shortName; 
        cnt = xlanguage::languageCount(); 
        for (i = 0; i<=cnt; i++) 
        { 
            languageID =xLanguage::index2languageID(i); 
            print "Language ", i, ":", languageID, ":"; 
        } 
        cnt = xLanguage::labelFileCount(); 
        for (i = 0; i<=cnt; i++) 
        { 
            shortName =xLanguage::labelFileNumber2LanguageID(i); 
            languageID =xLanguage::index2languageID(i); 
            description = xLanguage::languageID2Description(languageID); 
            print i, ":", shortName, ":", description; 
        } 
        pause; 
    }

### <a name="methods"></a>方法

| 方法                                                     | 説明                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| ::public static str index2languageID(int number)           | 指定された言語の言語 ID (たとえば、"en-us") を取得します。                                 |
| ::public static int labelFileCount()                       | ラベル ファイルの数を返します。                                                                          |
| ::public static str labelFileNumber2LanguageID(int number) |                                                                                                             |
| ::public static int languageCount()                        |                                                                                                             |
| ::public static str languageID2Description(str languageID) | 言語 ID が付与された、指定された言語 ("英語 (米国)" など) の名前を返されます。 |
| ::public static int languageID2LCID(str languageID)        |                                                                                                             |
| ::public static str lcid2languageID(int lcid)              |                                                                                                             |

### <a name="method-index2languageid"></a>メソッド index2languageID

指定された言語の言語 ID (たとえば、"en-us") を取得します。

    public static str index2languageID(int number)

#### <a name="parameters"></a>パラメーター

数値  
1 と languageCount メソッドの戻り値の間での番号。

#### <a name="return-value"></a>戻り値

言語 ID。

### <a name="method-labelfilecount"></a>メソッド labelFileCount

ラベル ファイルの数を返します。

    public static int labelFileCount()

#### <a name="return-value"></a>戻り値

ラベル ファイルの数 (つまり、ax???\*.ald という形式の名前を持つファイルの数)。

### <a name="method-labelfilenumber2languageid"></a>メソッド labelFileNumber2LanguageID

    public static str labelFileNumber2LanguageID(int number)

#### <a name="parameters"></a>パラメーター

数値  

#### <a name="return-value"></a>戻り値

### <a name="method-languagecount"></a>メソッド languageCount

    public static int languageCount()

#### <a name="return-value"></a>戻り値

### <a name="method-languageid2description"></a>メソッド languageID2Description

言語 ID が付与された、指定された言語 ("英語 (米国)" など) の名前を返されます。

    public static str languageID2Description(str languageID)

#### <a name="parameters"></a>パラメーター

languageID  
言語の ID (たとえば、"en-us")。

#### <a name="return-value"></a>戻り値

言語の説明を含む文字列。

### <a name="method-languageid2lcid"></a>メソッド languageID2LCID

    public static int languageID2LCID(str languageID)

#### <a name="parameters"></a>パラメーター

languageID  

#### <a name="return-value"></a>戻り値

### <a name="method-lcid2languageid"></a>メソッド lcid2languageID

    public static str lcid2languageID(int lcid)

#### <a name="parameters"></a>パラメーター

lcid  

#### <a name="return-value"></a>戻り値

## <a name="class-xmenufunction"></a>クラス xMenuFunction
    class xMenuFunction extends SecureNode

xMenuFunction クラスは、フォーム、レポート、ジョブ、クラス、クエリにアクセスして実行するための簡単な方法を提供する、他の Finance and Operations アプリケーション オブジェクトへのインターフェイスを表します。

### <a name="remarks"></a>備考

xMenuFunction オブジェクトとそのメソッドおよびプロパティを使用して、アプリケーション オブジェクトを参照します。 たとえば、次のことを実行できます。

-   Run メソッドを使用してプロパティで参照されるオブジェクトを実行する
-   xMenuFunction オブジェクトを作成し、そのオブジェクトが実行する (または参照する) オブジェクトへの参照を作成します。 これにより、オブジェクトを実行する前に渡された引数を操作できます

注記: このシステム クラスは、AOT 内の MenuItem ノードを表します。 このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                  | 説明                                                                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])                                                                     | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                                                                 | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                        |
| public str changedTime(\[str value\])                                                                   | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                        |
| public boolean checkAccessRights()                                                                      |                                                                                                                                           |
| public int copyCallerQuery(\[int value\])                                                               |                                                                                                                                           |
| public int correctPermissions(\[int value\])                                                            |                                                                                                                                           |
| public str countryRegionCodes(\[str value\])                                                            |                                                                                                                                           |
| public ObjectRun create(\[xArgs args\])                                                                 | Finance and Operations アプリケーション オブジェクトへの参照を作成し、返します。                                                           |
| public str createdBy(\[str value\])                                                                     | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public int createPermissions(\[int value\])                                                             |                                                                                                                                           |
| public Date creationDate(\[Date value\])                                                                | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                                                                  |                                                                                                                                           |
| public int deletePermissions(\[int value\])                                                             |                                                                                                                                           |
| public str disabledImage(\[str value\])                                                                 | コントロールの無効な画像を取得または設定します。                                                                                            |
| public int disabledImageLocation(\[int value\])                                                         |                                                                                                                                           |
| public int disabledResource(\[int value\])                                                              | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                            |
| public int enumParameter(\[int value\])                                                                 | MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。                               |
| public EnumId enumTypeParameter(\[EnumId value\])                                                       | MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。                                                                   |
| public int formViewOption(\[int value\])                                                                |                                                                                                                                           |
| public Query getRootQuery()                                                                             |                                                                                                                                           |
| public boolean hasRunPermissions(\[xArgs args\])                                                        | xMenuFunction オブジェクトに実行権限があり、run() が正常に呼び出されるかどうかをチェックします。                                          |
| public str helpText(\[str value\])                                                                      | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public int imageLocation(\[int value\])                                                                 |                                                                                                                                           |
| public str label(\[str value\])                                                                         | コントロールのラベルを取得または設定します。                                                                                                     |
| public str linkedPermissionObject(\[str value\])                                                        |                                                                                                                                           |
| public str linkedPermissionObjectChild(\[str value\])                                                   |                                                                                                                                           |
| public int linkedPermissionType(\[int value\])                                                          |                                                                                                                                           |
| public int maintainUserLicense(\[int value\])                                                           |                                                                                                                                           |
| public boolean multiSelect(\[boolean value\])                                                           |                                                                                                                                           |
| public str name(\[str value\])                                                                          | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int needsRecord(\[int value\])                                                                   |                                                                                                                                           |
| public str normalImage(\[str value\])                                                                   |                                                                                                                                           |
| public int normalResource(\[int value\])                                                                |                                                                                                                                           |
| public str object(\[str value\])                                                                        | MenuFunction クラスにより実行されるオブジェクトを取得または設定します。                                                                            |
| public int objectType(\[int value\])                                                                    |                                                                                                                                           |
| public int openMode(\[int value\])                                                                      |                                                                                                                                           |
| public Guid origin(\[Guid value\])                                                                      |                                                                                                                                           |
| public str parameters(\[str value\])                                                                    | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                    |
| public str query(\[str value\])                                                                         |                                                                                                                                           |
| public int readPermissions(\[int value\])                                                               |                                                                                                                                           |
| public str reportDesign(\[str value\])                                                                  |                                                                                                                                           |
| public int runOn(\[int value\])                                                                         |                                                                                                                                           |
| public MenuItemType type()                                                                              |                                                                                                                                           |
| public int updatePermissions(\[int value\])                                                             |                                                                                                                                           |
| public int viewUserLicense(\[int value\])                                                               |                                                                                                                                           |
| public str web(\[str value\])                                                                           |                                                                                                                                           |
| public int webAccess(\[int value\])                                                                     |                                                                                                                                           |
| public str webMenuItemName(\[str value\])                                                               |                                                                                                                                           |
| public str webPage(\[str value\])                                                                       |                                                                                                                                           |
| public boolean webSecureTransaction(\[boolean value\])                                                  |                                                                                                                                           |
| public void run(\[xArgs args\])                                                                         | xMenuFunction オブジェクトを実行します。                                                                                                            |
| ::public static void runCalled(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\]) |                                                                                                                                           |
| ::public static void runClient(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\]) |                                                                                                                                           |
| ::public static void runServer(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\]) |                                                                                                                                           |
| public void new(str Name, MenuItemType type)                                                            | xMenuFunction の名前と MenuItemType を xMenuFunction コンストラクターに渡して、新しい xMenuFunction オブジェクトを作成します。                     |
| public void AOTrun(\[xArgs args\])                                                                      | アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。                                                                  |

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-checkaccessrights"></a>メソッド checkAccessRights

    public boolean checkAccessRights()

#### <a name="return-value"></a>戻り値

### <a name="method-copycallerquery"></a>メソッド copyCallerQuery

    public int copyCallerQuery([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-correctpermissions"></a>メソッド correctPermissions

    public int correctPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-create"></a>メソッド create

Finance and Operations アプリケーション オブジェクトへの参照を作成し、返します。

    public ObjectRun create([xArgs args])

#### <a name="parameters"></a>パラメーター

args  
xArgs クラス オブジェクト。オプション。

#### <a name="return-value"></a>戻り値

Finance and Operations アプリケーション オブジェクトへの参照。

#### <a name="remarks"></a>備考

このメソッドは、アプリケーション オブジェクトの作成に使用されます。 返されるオブジェクトは、オブジェクト変数に割り当てられます。 init 関数は create 関数によって呼び出されることに注意してください。 したがって、それを呼び出すべきではありません。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-createpermissions"></a>メソッド createPermissions

    public int createPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-deletepermissions"></a>メソッド deletePermissions

    public int deletePermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-disabledimage"></a>メソッド disabledImage

コントロールの無効な画像を取得または設定します。

    public str disabledImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画像ファイルのフル ネーム。システムは GDI でサポートされているすべての画像形式をサポートしています。

#### <a name="remarks"></a>備考

このプロパティは、disabledResource プロパティ値に優先します。 これらのプロパティの両方が設定されている場合に使用されます。

### <a name="method-disabledimagelocation"></a>メソッド disabledImageLocation

    public int disabledImageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-disabledresource"></a>メソッド disabledResource

無効なボタン画像として使用する画像リソース ID を取得または設定します。

    public int disabledResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

無効なボタン画像として使用する画像リソース ID。 アイコンとビットマップ イメージの両方がサポートされます。

### <a name="method-enumparameter"></a>メソッド enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。

    public int enumParameter([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。

### <a name="method-enumtypeparameter"></a>メソッド enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。

    public EnumId enumTypeParameter([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスの enumTypeParameter プロパティ。

### <a name="method-formviewoption"></a>メソッド formViewOption

    public int formViewOption([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getrootquery"></a>メソッド getRootQuery

    public Query getRootQuery()

#### <a name="return-value"></a>戻り値

### <a name="method-hasrunpermissions"></a>メソッド hasRunPermissions

xMenuFunction オブジェクトに実行権限があり、run() が正常に呼び出されるかどうかをチェックします。

    public boolean hasRunPermissions([xArgs args])

#### <a name="parameters"></a>パラメーター

args  
run() メソッドに渡される xArgs クラス オブジェクト。オプション。

#### <a name="return-value"></a>戻り値

run() を正常に呼び出すために必要なアクセス許可が存在する場合は true。

#### <a name="remarks"></a>備考

この関数は、アクセス許可が失敗した場合にスローされることがあります。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-linkedpermissionobject"></a>メソッド linkedPermissionObject

    public str linkedPermissionObject([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissionobjectchild"></a>メソッド linkedPermissionObjectChild

    public str linkedPermissionObjectChild([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-linkedpermissiontype"></a>メソッド linkedPermissionType

    public int linkedPermissionType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-maintainuserlicense"></a>メソッド maintainUserLicense

    public int maintainUserLicense([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-multiselect"></a>メソッド multiSelect

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-needsrecord"></a>メソッド needsRecord

    public int needsRecord([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalresource"></a>メソッド normalResource

    public int normalResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-object"></a>メソッド object

MenuFunction クラスにより実行されるオブジェクトを取得または設定します。

    public str object([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

MenuFunction クラスにより実行されるオブジェクト。

#### <a name="remarks"></a>備考

プロパティ値は、次のオブジェクトのいずれかである場合があります。

-   フォーム。
-   レポート。
-   ジョブ。
-   クラス。
-   クエリ。

### <a name="method-objecttype"></a>メソッド objectType

    public int objectType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-openmode"></a>メソッド openMode

    public int openMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-query"></a>メソッド query

    public str query([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-readpermissions"></a>メソッド readPermissions

    public int readPermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-reportdesign"></a>メソッド reportDesign

    public str reportDesign([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-runon"></a>メソッド runOn

    public int runOn([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public MenuItemType type()

#### <a name="return-value"></a>戻り値

### <a name="method-updatepermissions"></a>メソッド updatePermissions

    public int updatePermissions([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-viewuserlicense"></a>メソッド viewUserLicense

    public int viewUserLicense([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-web"></a>メソッド web

    public str web([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webaccess"></a>メソッド webAccess

    public int webAccess([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webmenuitemname"></a>メソッド webMenuItemName

    public str webMenuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webpage"></a>メソッド webPage

    public str webPage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-websecuretransaction"></a>メソッド webSecureTransaction

    public boolean webSecureTransaction([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-run"></a>メソッド run

xMenuFunction オブジェクトを実行します。

    public void run([xArgs args])

#### <a name="parameters"></a>パラメーター

args  
xArgs クラス オブジェクト。オプション。

#### <a name="remarks"></a>備考

この関数は、コードから xMenuFunction オブジェクトを実行するために使用されます。

### <a name="method-runcalled"></a>メソッド runCalled

    public static void runCalled(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])

#### <a name="parameters"></a>パラメーター

氏名  

<!-- -->

タイプ  

<!-- -->

setContextMenu  

<!-- -->

args  

### <a name="method-runclient"></a>メソッド runClient

    public static void runClient(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])

#### <a name="parameters"></a>パラメーター

氏名  

<!-- -->

タイプ  

<!-- -->

setContextMenu  

<!-- -->

args  

### <a name="method-runserver"></a>メソッド runServer

    public static void runServer(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])

#### <a name="parameters"></a>パラメーター

氏名  

<!-- -->

タイプ  

<!-- -->

setContextMenu  

<!-- -->

args  

### <a name="method-new"></a>メソッド new

xMenuFunction の名前と MenuItemType を xMenuFunction コンストラクターに渡して、新しい xMenuFunction オブジェクトを作成します。

    public void new(str Name, MenuItemType type)

#### <a name="parameters"></a>パラメーター

氏名  
MenuItemType システム列挙型の定数: MenuItemType::Display、MenuItemType::Output、または MenuItemType::Action。

<!-- -->

タイプ  
MenuItemType システム列挙型の定数: MenuItemType::Display、MenuItemType::Output、または MenuItemType::Action。

#### <a name="remarks"></a>備考

xMenuFunction オブジェクトを作成するとき、パラメータは既存の xMenuFunction を一意に識別する必要があります。 それ以外の場合は、Exception::Internal がスローされます。

### <a name="method-aotrun"></a>メソッド AOTrun

アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

    public void AOTrun([xArgs args])

#### <a name="parameters"></a>パラメーター

args  

## <a name="class-xnavpane"></a>クラス xNavPane
    class xNavPane extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                | 説明                                       |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| public boolean collapseFavoriteNode(str path)                                                         |                                                   |
| public boolean collapseNode(str path)                                                                 |                                                   |
| public boolean expandFavoriteNode(str path)                                                           |                                                   |
| public boolean expandNode(str path)                                                                   |                                                   |
| public boolean favPaneVisible(\[boolean value\])                                                      |                                                   |
| public container getButtons()                                                                         |                                                   |
| public str getCurrMenuName()                                                                          |                                                   |
| public TreeNode getSelectedFavoriteNode()                                                             |                                                   |
| public TreeNode getSelectedNode()                                                                     |                                                   |
| public boolean navPaneVisible(\[boolean value\])                                                      |                                                   |
| public boolean runFavoriteNode(str path)                                                              |                                                   |
| public boolean runNode(str path)                                                                      |                                                   |
| public str selectedFavoriteGroup(\[str groupName\])                                                   |                                                   |
| public str selectedGroup(\[str groupName\])                                                           |                                                   |
| public boolean setSelectedFavoriteNode(str path)                                                      |                                                   |
| public boolean setSelectedNode(str path)                                                              |                                                   |
| public void refreshFavorites(\[str selectFavoriteGroup\], \[int workspaceNum\], \[boolean saveToDB\]) |                                                   |
| public void setCurrMenuButtons(container buttons)                                                     |                                                   |
| public void loadStartupButtons()                                                                      |                                                   |
| public void new()                                                                                     | xNavPane クラスの新しいインスタンスを初期化します。 |

### <a name="method-collapsefavoritenode"></a>メソッド collapseFavoriteNode

    public boolean collapseFavoriteNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-collapsenode"></a>メソッド collapseNode

    public boolean collapseNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-expandfavoritenode"></a>メソッド expandFavoriteNode

    public boolean expandFavoriteNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-expandnode"></a>メソッド expandNode

    public boolean expandNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-favpanevisible"></a>メソッド favPaneVisible

    public boolean favPaneVisible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getbuttons"></a>メソッド getButtons

    public container getButtons()

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrmenuname"></a>メソッド getCurrMenuName

    public str getCurrMenuName()

#### <a name="return-value"></a>戻り値

### <a name="method-getselectedfavoritenode"></a>メソッド getSelectedFavoriteNode

    public TreeNode getSelectedFavoriteNode()

#### <a name="return-value"></a>戻り値

### <a name="method-getselectednode"></a>メソッド getSelectedNode

    public TreeNode getSelectedNode()

#### <a name="return-value"></a>戻り値

### <a name="method-navpanevisible"></a>メソッド navPaneVisible

    public boolean navPaneVisible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-runfavoritenode"></a>メソッド runFavoriteNode

    public boolean runFavoriteNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-runnode"></a>メソッド runNode

    public boolean runNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-selectedfavoritegroup"></a>メソッド selectedFavoriteGroup

    public str selectedFavoriteGroup([str groupName])

#### <a name="parameters"></a>パラメーター

groupName  

#### <a name="return-value"></a>戻り値

### <a name="method-selectedgroup"></a>メソッド selectedGroup

    public str selectedGroup([str groupName])

#### <a name="parameters"></a>パラメーター

groupName  

#### <a name="return-value"></a>戻り値

### <a name="method-setselectedfavoritenode"></a>メソッド setSelectedFavoriteNode

    public boolean setSelectedFavoriteNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-setselectednode"></a>メソッド setSelectedNode

    public boolean setSelectedNode(str path)

#### <a name="parameters"></a>パラメーター

path  

#### <a name="return-value"></a>戻り値

### <a name="method-refreshfavorites"></a>メソッド refreshFavorites

    public void refreshFavorites([str selectFavoriteGroup], [int workspaceNum], [boolean saveToDB])

#### <a name="parameters"></a>パラメーター

selectFavoriteGroup  

<!-- -->

workspaceNum  

<!-- -->

saveToDB  

### <a name="method-setcurrmenubuttons"></a>メソッド setCurrMenuButtons

    public void setCurrMenuButtons(container buttons)

#### <a name="parameters"></a>パラメーター

buttons  

### <a name="method-loadstartupbuttons"></a>メソッド loadStartupButtons

    public void loadStartupButtons()

### <a name="method-new"></a>メソッド new

xNavPane クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-xppcompiler"></a>クラス XppCompiler
    class XppCompiler extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                 | 説明                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| public boolean compile(str source)     |                                                                                                                   |
| public boolean compileExpr(str source) |                                                                                                                   |
| public str dumpClass(str className)    | クラスの X++ コンパイラ情報を含む XML 文字列を作成します。                                     |
| public str dumpEnums()                 | 現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報を含む XML 文字列を作成します。 |
| public str dumpTable(str tableName)    | テーブルの X++ コンパイラ情報を含む XML 文字列を作成します。                                     |
| public str errorText()                 |                                                                                                                   |
| public AnyType execute(VarArg )        |                                                                                                                   |
| public AnyType executeEx()             |                                                                                                                   |
| public void setGuidArg(Guid arg)       |                                                                                                                   |
| public void setInt64Arg(Int64 arg)     |                                                                                                                   |
| public void setDateArg(Date arg)       |                                                                                                                   |
| public void new()                      | XppCompiler クラスの新しいインスタンスを初期化します。                                                              |
| public void endArgs()                  |                                                                                                                   |
| public void startArgs()                |                                                                                                                   |
| public void setRealArg(Real arg)       |                                                                                                                   |
| public void setIntArg(int arg)         |                                                                                                                   |
| public void setStrArg(str arg)         |                                                                                                                   |

### <a name="method-compile"></a>メソッド compile

    public boolean compile(str source)

#### <a name="parameters"></a>パラメーター

ソース  

#### <a name="return-value"></a>戻り値

### <a name="method-compileexpr"></a>メソッド compileExpr

    public boolean compileExpr(str source)

#### <a name="parameters"></a>パラメーター

ソース  

#### <a name="return-value"></a>戻り値

### <a name="method-dumpclass"></a>メソッド dumpClass

クラスの X++ コンパイラ情報を含む XML 文字列を作成します。

    public str dumpClass(str className)

#### <a name="parameters"></a>パラメーター

className  

#### <a name="return-value"></a>戻り値

指定したクラスの X++ コンパイラ情報

#### <a name="remarks"></a>備考

バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。

### <a name="method-dumpenums"></a>メソッド dumpEnums

現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報を含む XML 文字列を作成します。

    public str dumpEnums()

#### <a name="return-value"></a>戻り値

現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報

#### <a name="remarks"></a>備考

バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。

### <a name="method-dumptable"></a>メソッド dumpTable

テーブルの X++ コンパイラ情報を含む XML 文字列を作成します。

    public str dumpTable(str tableName)

#### <a name="parameters"></a>パラメーター

tableName  

#### <a name="return-value"></a>戻り値

指定したテーブルの X++ コンパイラ情報

#### <a name="remarks"></a>備考

バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。

### <a name="method-errortext"></a>メソッド errorText

    public str errorText()

#### <a name="return-value"></a>戻り値

### <a name="method-execute"></a>メソッド execute

    public AnyType execute(VarArg )

#### <a name="parameters"></a>パラメーター



#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

XppCompiler オブジェクトは実行時にコードをコンパイルすることができます。 これはセキュリティ リスクをもたらします。 したがって、メソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

次の例では、execute メソッドを呼び出して、指定されたバッファをコンパイルして実行します。

    void XppCompilerExecuteExample(Common _buf) 
    { 
        XppCompiler       xpp; 
        ExecutePermission perm; 
        perm = new ExecutePermission(); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
        xpp = new XppCompiler(); 
        if (xpp != null) 
        { 
            xpp.execute(_buf); 
        } 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-executeex"></a>メソッド executeEx

    public AnyType executeEx()

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

XppCompiler オブジェクトは実行時にコードをコンパイルすることができます。 これはセキュリティ リスクをもたらします。 したがって、executeEx メソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

    void XppCompilerExecuteExExample() 
    { 
        XppCompiler       xpp; 
        ExecutePermission perm; 
        perm = new ExecutePermission(); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
        xpp = new XppCompiler(); 
        if (xpp != null) 
        { 
            xpp.executeEx(); 
        } 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-setguidarg"></a>メソッド setGuidArg

    public void setGuidArg(Guid arg)

#### <a name="parameters"></a>パラメーター

arg  

### <a name="method-setint64arg"></a>メソッド setInt64Arg

    public void setInt64Arg(Int64 arg)

#### <a name="parameters"></a>パラメーター

arg  

### <a name="method-setdatearg"></a>メソッド setDateArg

    public void setDateArg(Date arg)

#### <a name="parameters"></a>パラメーター

arg  

### <a name="method-new"></a>メソッド new

XppCompiler クラスの新しいインスタンスを初期化します。

    public void new()

#### <a name="remarks"></a>備考

XppCompiler クラスのインスタンスは、実行時にコードをコンパイルできます。 これはセキュリティ リスクを提示するため、新しいメソッドはコード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。

### <a name="method-endargs"></a>メソッド endArgs

    public void endArgs()

### <a name="method-startargs"></a>メソッド startArgs

    public void startArgs()

### <a name="method-setrealarg"></a>メソッド setRealArg

    public void setRealArg(Real arg)

#### <a name="parameters"></a>パラメーター

arg  

### <a name="method-setintarg"></a>メソッド setIntArg

    public void setIntArg(int arg)

#### <a name="parameters"></a>パラメーター

arg  

### <a name="method-setstrarg"></a>メソッド setStrArg

    public void setStrArg(str arg)

#### <a name="parameters"></a>パラメーター

arg  

## <a name="class-xppprepostargs"></a>クラス XppPrePostArgs
    class XppPrePostArgs extends XppEventArgs

XppPrePostArgs クラスは、プリハンドラーとポストハンドラーのためのパブリッシャーの引数と戻り値に関する情報を提供します。

### <a name="remarks"></a>備考

パブリッシャーは、プリイベントとポストイベントを公開するメソッドです。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public boolean wrapper(str fieldName, AnyType value)                                         |                                                                                                             |
| public struct args()                                                                         |                                                                                                             |
| public boolean existsArg(str fieldName)                                                      | 出版社の引数の存在を名前でチェックします。                                                   |
| public AnyType getArgNum(int argIndex)                                                       | パブリッシャーの引数をインデックスごとに取得します。                                                               |
| public int setArgNum(int argIndex, AnyType value)                                            | パブリッシャーの引数をインデックスごとに設定します。                                                                     |
| public AnyType value(str fieldName)                                                          |                                                                                                             |
| public XppEventHandlerCalledWhen getCalledWhen()                                             | プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを示す値を取得します。 |
| public AnyType getReturnValue()                                                              | 発行元の戻り値を取得します。                                                                          |
| public AnyType getThis()                                                                     | 発行元の「this」参照を取得します。                                                                      |
| public boolean removeArg(str fieldName)                                                      |                                                                                                             |
| public int wrapper(str fieldName, AnyType value)                                             |                                                                                                             |
| public int setReturnValue(AnyType retval)                                                    | 発行元の戻り値を設定します。                                                                          |
| public str isFirst()                                                                         |                                                                                                             |
| public void setCalledWhen(XppEventHandlerCalledWhen calledWhen)                              | プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを設定します。                             |
| ::public static void setReturnValueEx(AnyType retval, XppPrePostArgs args)                   |                                                                                                             |
| public void new(\[AnyType thisPtr\], \[str args\], \[XppEventHandlerCalledWhen calledWhen\]) | Object クラスの新しいインスタンスを初期化します。                                                             |

### <a name="method-wrapper"></a>メソッド wrapper

    public boolean wrapper(str fieldName, AnyType value)

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-args"></a>メソッド args

    public struct args()

#### <a name="return-value"></a>戻り値

### <a name="method-existsarg"></a>メソッド existsArg

出版社の引数の存在を名前でチェックします。

    public boolean existsArg(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

指定された引数が存在するかどうかを示すブール値データ型。

#### <a name="remarks"></a>備考

引数名は大文字と小文字を区別しません。

### <a name="method-getargnum"></a>メソッド getArgNum

パブリッシャーの引数をインデックスごとに取得します。

    public AnyType getArgNum(int argIndex)

#### <a name="parameters"></a>パラメーター

argIndex  
ターゲット引数の int インデックス。

#### <a name="return-value"></a>戻り値

指定された引数の anytype 値です。

#### <a name="remarks"></a>備考

インデックスの範囲は、静的パブリッシャーの場合は 0 ベース、インスタンス パブリッシャーの場合は 1 ベースです。

### <a name="method-setargnum"></a>メソッド setArgNum

パブリッシャーの引数をインデックスごとに設定します。

    public int setArgNum(int argIndex, AnyType value)

#### <a name="parameters"></a>パラメーター

argIndex  
指定された引数に割り当てる anytype 値です。

<!-- -->

値  
指定された引数に割り当てる anytype 値です。

#### <a name="return-value"></a>戻り値

int データ型値 1 。

#### <a name="remarks"></a>備考

インデックスの範囲は、静的パブリッシャーの場合は 0 ベース、インスタンス パブリッシャーの場合は 1 ベースです。

### <a name="method-value"></a>メソッド value

    public AnyType value(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-getcalledwhen"></a>メソッド getCalledWhen

プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを示す値を取得します。

    public XppEventHandlerCalledWhen getCalledWhen()

#### <a name="return-value"></a>戻り値

XppPrePostArgs インスタンスはプリハンドラーまたはポストハンドラーかどうかを示す XppEventHandlerCalledWhen データ型値です。

### <a name="method-getreturnvalue"></a>メソッド getReturnValue

発行元の戻り値を取得します。

    public AnyType getReturnValue()

#### <a name="return-value"></a>戻り値

anytype データ型値は、発行元の戻り値を表します。

#### <a name="remarks"></a>備考

このメソッドは、プリハンドラー用ではありません。

### <a name="method-getthis"></a>メソッド getThis

発行元の「this」参照を取得します。

    public AnyType getThis()

#### <a name="return-value"></a>戻り値

anytype データ型値は、発行元の「this」参照を表します。

#### <a name="remarks"></a>備考

パブリッシャーが静的な場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなしになる) を返します。

### <a name="method-removearg"></a>メソッド removeArg

    public boolean removeArg(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-wrapper"></a>メソッド wrapper

    public int wrapper(str fieldName, AnyType value)

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-setreturnvalue"></a>メソッド setReturnValue

発行元の戻り値を設定します。

    public int setReturnValue(AnyType retval)

#### <a name="parameters"></a>パラメーター

retval  

#### <a name="return-value"></a>戻り値

int データ型値 1 。

#### <a name="remarks"></a>備考

このメソッドは、プリハンドラーまたは無効を返すパブリッシャーのためのものではありません。

### <a name="method-isfirst"></a>メソッド isFirst

    public str isFirst()

#### <a name="return-value"></a>戻り値

### <a name="method-setcalledwhen"></a>メソッド setCalledWhen

プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを設定します。

    public void setCalledWhen(XppEventHandlerCalledWhen calledWhen)

#### <a name="parameters"></a>パラメーター

calledWhen  

#### <a name="remarks"></a>備考

このメソッドは、プリハンドラーまたはポストハンドラーのコードから明示的に呼び出されてはなりません。 このメソッドは、単体テストおよび自動生成コード用に予約されています。

### <a name="method-setreturnvalueex"></a>メソッド setReturnValueEx

    public static void setReturnValueEx(AnyType retval, XppPrePostArgs args)

#### <a name="parameters"></a>パラメーター

retval  

<!-- -->

args  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new([AnyType thisPtr], [str args], [XppEventHandlerCalledWhen calledWhen])

#### <a name="parameters"></a>パラメーター

thisPtr  

<!-- -->

args  

<!-- -->

calledWhen  

## <a name="class-xrecord"></a>クラス xRecord
    class xRecord extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                     | 説明                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| public boolean aosValidateDelete()                                                                                         | サーバー上で、指定されたレコードをテーブルから削除できることを検証します。                                                 |
| public boolean aosValidateInsert()                                                                                         | サーバー上で、指定されたレコードを挿入できることを検証します。                                                             |
| public boolean aosValidateRead()                                                                                           | サーバー上で、指定されたレコードを読み取れることを検証します。                                                                 |
| public boolean aosValidateUpdate()                                                                                         | サーバー上で、指定されたレコードを更新できることを検証します。                                                              |
| public container buf2con(\[boolean packOrigBuffer\])                                                                       | X++ コンテナーに xRecord インスタンスのテーブル バッファーをパックします。                                                          |
| public boolean canSubmitToWorkflow(\[str workflowType\])                                                                   | ワークフローへの送信が可能かどうかを示します。                                                                          |
| public str caption()                                                                                                       | テーブルのキャプション プロパティを取得および設定します。                                                                                 |
| public boolean checkInvalidFieldAccess(\[boolean checkInvalidFieldAccess\])                                                | 無効なフィールド アクセスを取得および設定します。                                                                                            |
| public boolean checkRecord(\[boolean checkMandatoryFields\])                                                               | 必須フィールドをチェックするかどうかを示すプロパティを取得および設定します。                                                   |
| public boolean checkRestrictedDeleteActions(\[boolean checkRestrictedDeleteActions\])                                      | レコードが削除されるかどうかを示すプロパティを取得および設定します。                                                     |
| public SelectableDataArea company(\[SelectableDataArea company\])                                                          | レコードの法人を示すプロパティを取得および設定します。                                                       |
| public Common con2buf(container container)                                                                                 | コンテナをテーブル バッファに展開します。                                                                                    |
| public ConcurrencyModel concurrencyModel(\[ConcurrencyModel concurrencyModel\])                                            | レコードの更新に使用する既定の同時実行モデルを取得および設定します。                                                          |
| public int context(\[int newValue\])                                                                                       | コンテキスト プロパティを取得および設定します。                                                                                            |
| public Common data(\[Common cursor\])                                                                                      | テーブルから行を取得します。                                                                                                |
| public FormObjectSet dataSource()                                                                                          | テーブルのデータ ソースを取得します。                                                                                        |
| public boolean disableCache(\[boolean newValue\])                                                                          | キャッシュが無効かどうかを示すプロパティを取得および設定します。                                                         |
| public boolean doValidateDelete()                                                                                          | レコードを削除できる検証するアクションを実行します。                                                                  |
| public boolean equal(Common cursor)                                                                                        | 指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。                                                           |
| public AccessRight fieldAccessRight(FieldName fieldName)                                                                   | フィールドのアクセス権を返します。                                                                                                |
| public AccessRight fieldBufferAccessRight(FieldName fieldName)                                                             | 現在のレコードのフィールド アクセス権を返します。                                                                         |
| public FieldState fieldState(FieldId fieldId, \[FieldState state\])                                                        | テーブル バッファーのフィールドの状態を設定するか返します。                                                                      |
| public container getAllowRedefault()                                                                                       | 既定値に再度設定することを許可されているフィールドの一覧を返します。                                                                     |
| public container getDefaultingDependencies()                                                                               | デフォルトの依存関係を保持するコンテナーを返します。                                                                      |
| public TableExtension getExtension()                                                                                       | テーブル拡張機能を返します。                                                                                                   |
| public AnyType getFieldValue(str fieldName, \[int arrayIndex\])                                                            | テーブル バッファから指定したフィールドの値を取得します。                                                                     |
| public str getInstanceRelationType()                                                                                       | InstanceRelationType ID に対応するテーブルの名前を返します。                                                        |
| public str getPhysicalTableName()                                                                                          | 物理テーブル名を返します。SQL Temp DB テーブルの場合は、テーブル インスタンス名です。                       |
| public PresenceInfo getPresenceFieldData(FieldId fieldId, AnyType fieldValue)                                              | 指定されたフィールドから PresenceInfo 値を取得します。                                                                     |
| public str getSQLStatement()                                                                                               | レコードをデータベースから取得するために使用される SQL ステートメントを取得します。                                                       |
| public Common getTableInInstanceHierarchy(TableId tableId)                                                                 |                                                                                                                                |
| public TableType getTableType()                                                                                            | テーブルのタイプを示します。                                                                                               |
| public boolean hasRelatedTable(str relatedRoleName)                                                                        | 外部キー制約バッファがテーブルにリンクされているかどうかを示します。                                                    |
| public str helpField(FieldId fieldId)                                                                                      | 指定したフィールドのヘルプ テキストを含む文字列を取得します。                                                        |
| public FieldState inputStatus(\[FieldState inputStatus\])                                                                  | テーブル バッファーの現在の入力ステータスを設定するか返します。                                                                  |
| public boolean interactiveContext(\[boolean context\])                                                                     | テーブル バッファーの現在のインタラクティブ コンテキストを設定するか返します。                                                           |
| public boolean isFieldDataRetrieved(str fieldName, \[int arrayIndex\])                                                     | 指定されたフィールドのデータが取得されたかどうかをチェックします。                                                                 |
| public boolean isFieldSet(FieldId fieldId)                                                                                 | フィールドがセットまたは既定状態かどうかをチェックします。                                                                           |
| public boolean isFormDataSource()                                                                                          | データ ソースがフォームであるかどうかを示します。                                                                                   |
| public boolean isNewRecord()                                                                                               | レコードがまだ保存されていない新しいレコードである場合は true を返します。                                                     |
| public boolean isPartOfUOWSaveChanges()                                                                                    |                                                                                                                                |
| public boolean isTempDb()                                                                                                  | テーブルのタイプが SQL TempDB であるかどうかを示します。                                                                         |
| public boolean isTmp()                                                                                                     | これが一時テーブルであるかどうかを示します。                                                                                   |
| public Common joinChild()                                                                                                  | 現在のレコードの結合子を検索します。                                                                                    |
| public Common joinParent()                                                                                                 | 現在のレコードの結合の親を検索します。                                                                                   |
| public boolean linkPhysicalTableInstance(\[Common record\])                                                                | レコードの物理テーブル インスタンスへのリンクがあるかどうかを確認します。                                                 |
| public Common orig()                                                                                                       | 現在のレコードの元の値を取得します。                                                                           |
| public boolean overwriteSystemfields(\[boolean allowOverwrite\])                                                           | システム フィールドを上書きできるかどうかを示すプロパティを取得および設定します。                                            |
| public boolean queryTimedOut()                                                                                             | クエリが実行の時間制限を超過したかどうかを示します。                                                             |
| public int queryTimeout(\[int seconds\], \[boolean raiseException\])                                                       | クエリの実行に対する時間制限を示すプロパティを取得および設定します。                                         |
| public boolean readCommittedLock(\[boolean readCommittedLock\])                                                            |                                                                                                                                |
| public boolean readPast(\[boolean skipLockedRows\])                                                                        | レコードの読み取り時に、他のプロセスによりロックされる行をスキップするかどうかを示すプロパティを取得および設定します。       |
| public boolean recordLevelSecurity(\[boolean newValue\])                                                                   | レコード レベルのセキュリティを適用するかどうかを示すプロパティを取得および設定します。                                         |
| public Common relatedTable(str name, \[Common buffer\])                                                                    | テーブル バッファのリンクに関連するバッファーを設定するか返します。                                                                |
| public Int64 RowCount()                                                                                                    | テーブル内の行数を取得します。                                                                                     |
| public boolean selectForUpdate(\[boolean lockRecordsExclusive\])                                                           | 読み取り時に更新用のレコードを選択するかどうかを示すプロパティを取得および設定します。                             |
| public boolean selectLocked(\[boolean lockRecordsShared\])                                                                 | ロックされているレコードを選択するかどうかを示します。                                                                                    |
| public Common selectRefRecord(FieldId referenceFieldId)                                                                    | 参照されているフィールド ID によりレコードを選択します。                                                                                     |
| public boolean selectWithRepeatableRead(\[boolean useRepeatableRead\])                                                     | 反復可能な読み取りが有効かどうかを示すプロパティを取得および設定します。                                                  |
| public boolean setTempDB()                                                                                                 |                                                                                                                                |
| public boolean setTmp()                                                                                                    | データベースに保存されていない場合にテーブルを設定します。                                                                    |
| public boolean skipAosValidation(\[boolean newValue\])                                                                     | Finance and Operations Application Object Server (AOS) の検証をスキップするかどうかを示すプロパティを取得および設定します。 |
| public boolean skipDatabaseLog(\[boolean newValue\])                                                                       | データベース ログ要求をスキップするかどうかを示すプロパティを取得および設定します。                                               |
| public boolean skipDataMethods(\[boolean newValue\])                                                                       | オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。                                               |
| public boolean skipDeleteActions(\[boolean newValue\])                                                                     | テーブルで削除アクションをスキップするかどうかを示すプロパティを取得および設定します。                                         |
| public boolean skipDeleteMethod(\[boolean newValue\])                                                                      | オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。                                               |
| public boolean skipEvents(\[boolean newValue\])                                                                            | xRecord オブジェクトの有効期間の Application.event\* メソッドの呼び出しをオフにするオプションを提供します。                  |
| public boolean skipPostLoad(\[boolean newValue\])                                                                          | テーブルで xRecord.postLoad メソッドの実行をスキップするかどうかを示すプロパティを取得および設定します。                  |
| public boolean skipTTSCheck(\[boolean newValue\])                                                                          | 更新用にレコードが選択されているかどうかを決定するため、チェックをスキップするかどうかを示すプロパティを取得および設定します。    |
| public boolean suppressWarnings(\[boolean newValue\])                                                                      | このポインタの警告を非表示にするかどうかを示すプロパティを取得および設定します。                                       |
| public AccessRight tableAccessRight()                                                                                      | テーブルのアクセス権を返します。                                                                                                |
| public AccessRight tableBufferAccessRight()                                                                                | 現在のレコードのテーブル アクセス権を返します。                                                                         |
| public boolean takeOwnershipOfTempDBTable(boolean newValue)                                                                |                                                                                                                                |
| public str toolTipField(FieldId fieldId)                                                                                   | 指定されたフィールドの HelpText 値を取得します。                                                                          |
| public str toolTipRecord()                                                                                                 | 現在のレコードのツールヒント値を取得します。                                                                            |
| public int usageCount()                                                                                                    | オブジェクトが持つ参照 (参照カウンターの値) の現在の番号を取得します。                           |
| public boolean useExistingTempDBTable(str physicalTempTableName)                                                           |                                                                                                                                |
| public boolean validateDelete()                                                                                            | 現在のレコードが有効で、データベースから削除する準備ができているかどうかを調べます。                                      |
| public boolean validateField(FieldId fieldIdToCheck)                                                                       | 指定されたフィールドが有効かどうかを判定します。                                                                               |
| public boolean validateFieldValue(FieldName fieldName, \[int arrayIndex\])                                                 |                                                                                                                                |
| private container validateRelations(\[boolean onlyValidateCompositeRelations\], \[boolean onlyValidateModifiedRelations\]) |                                                                                                                                |
| public boolean validateWrite()                                                                                             | 現在のレコードが有効で、書き込み可能な状態かどうかを判別します。                                                        |
| public ValidTimeStateUpdate validTimeStateUpdateMode(ValidTimeStateUpdate validTimeStateUpdateMode)                        | カーソルで有効な時間状態更新モードを設定します。                                                                             |
| public CachedHow wasCached()                                                                                               | データの取得元となった場所を指定します。                                                                      |
| public str xml(\[int indent\])                                                                                             | 現在のオブジェクトを表す XML 文字列を取得します。                                                                    |
| public void doDelete()                                                                                                     | 現在のレコードをテーブルから削除し、テーブルの delete メソッドの追加ロジックをバイパスします。                 |
| public void update()                                                                                                       | 現在のレコードを更新します。                                                                                                    |
| public void merge(Common mergeInto)                                                                                        | 現在のテーブルを指定されたテーブルとマージします。                                                                             |
| public void clear()                                                                                                        | テーブル バッファーからすべての行を削除します。                                                                                        |
| public void setXDSContext(\[str contextString\])                                                                           | 新しい XDS コンテキストを設定します。                                                                                                          |
| public void renamePrimaryKey()                                                                                             | この表の対応する主キーの値の変更に従って、他のテーブルの外部キーの名前を変更します。         |
| public void dispose()                                                                                                      | XRecord オブジェクトによって使用されているリソースを解放します。                                                                        |
| public void setConnection(Connection connection)                                                                           | この表のユーザー接続を設定します。                                                                                       |
| public void delete()                                                                                                       | テーブルから現在のレコードを削除します。                                                                                     |
| public void defaultField(FieldId fieldId)                                                                                  | テーブルのフィールドの既定値を設定します。                                                                              |
| private void dbOpInTransaction(\[boolean isWriteOperation\])                                                               | 失敗した場合にデータベース操作が正しく閉じられていることを確認します。                                                         |
| public void write()                                                                                                        | レコードが存在する場合は更新します。存在しない場合はレコードを挿入します。                                                                    |
| public void preRemoting()                                                                                                  | 他のレベルに状態をパックしているテーブルに対してレベル間の呼び出しが実行される前に実行されます。        |
| public void modifiedFieldValue(FieldName fieldName, \[int arrayIndex\])                                                    | 指定したフィールドを元の値に変更します。                                                                            |
| public void defaultRow()                                                                                                   | 非対話型の場合、テーブルのフィールドの既定値を設定します。                                                   |
| public void reread()                                                                                                       | テーブルからレコードを再読み取りします。                                                                                             |
| public void modifiedField(FieldId fieldId)                                                                                 | 指定したフィールドを元通りに変更します。                                                                                  |
| public void ttsabort()                                                                                                     | ttsbegin メソッドの呼び出しによって開始されたトランザクションの廃棄。                                                        |
| public void insert()                                                                                                       | テーブルにレコードを挿入します。                                                                                             |
| public void doClear()                                                                                                      | 現在の行をテーブル バッファーから削除し、テーブルの clear メソッドの追加ロジックをバイパスします。                     |
| public void initValue()                                                                                                    | フィールドを既定値に初期化します。                                                                                      |
| public void doUpdate()                                                                                                     | 現在のレコードを更新し、テーブルの更新メソッドにある追加ロジックをバイパスします。                                |
| public void ttsbegin()                                                                                                     | ttscommit メソッドによりコミット、または ttsabort メソッドによって中止できるトランザクションを開始します。                   |
| public void setCrossPartition(boolean newValue)                                                                            | テーブルのパーティション間分割を設定またはリセットします。                                                                               |
| public void setTmpData(Common cursor)                                                                                      | 一時的なテーブルの内容を指定されたデータに設定します。                                                                |
| public void ttscommit()                                                                                                    | ttsbegin メソッドの呼び出しによって開始されたトランザクションをコミットします。                                                       |
| public void setFieldValue(str fieldName, AnyType value, \[int arrayIndex\])                                                | レコード バッファーのフィールド値を設定します。                                                                                     |
| public void doInsert()                                                                                                     | テーブルにレコードを挿入し、テーブルの挿入メソッドで追加のロジックをバイパスします。                         |
| public void setSQLTracing(\[boolean tracingmode\])                                                                         | SQL トレース モードを有効または無効にします。                                                                                          |
| public void postLoad()                                                                                                     | レコードが読み取られた後に実行されます。                                                                                            |

### <a name="method-aosvalidatedelete"></a>メソッド aosValidateDelete

サーバー上で、指定されたレコードをテーブルから削除できることを検証します。

    public boolean aosValidateDelete()

#### <a name="return-value"></a>戻り値

レコードを削除することができる場合は true。それ以外の場合は、false。

### <a name="method-aosvalidateinsert"></a>メソッド aosValidateInsert

サーバー上で、指定されたレコードを挿入できることを検証します。

    public boolean aosValidateInsert()

#### <a name="return-value"></a>戻り値

レコードを挿入することができる場合は true。それ以外の場合は、false。

### <a name="method-aosvalidateread"></a>メソッド aosValidateRead

サーバー上で、指定されたレコードを読み取れることを検証します。

    public boolean aosValidateRead()

#### <a name="return-value"></a>戻り値

レコードを読み取ることができる場合は true。それ以外の場合は、false。

### <a name="method-aosvalidateupdate"></a>メソッド aosValidateUpdate

サーバー上で、指定されたレコードを更新できることを検証します。

    public boolean aosValidateUpdate()

#### <a name="return-value"></a>戻り値

レコードを更新することができる場合は true。それ以外の場合は、false。

### <a name="method-buf2con"></a>メソッド buf2con

X++ コンテナーに xRecord インスタンスのテーブル バッファーをパックします。

    public container buf2con([boolean packOrigBuffer])

#### <a name="parameters"></a>パラメーター

packOrigBuffer  

#### <a name="return-value"></a>戻り値

梱包済みバッファーを保持するコンテナーです。

### <a name="method-cansubmittoworkflow"></a>メソッド canSubmitToWorkflow

ワークフローへの送信が可能かどうかを示します。

    public boolean canSubmitToWorkflow([str workflowType])

#### <a name="parameters"></a>パラメーター

workflowType  

#### <a name="return-value"></a>戻り値

送信が可能な場合は true。それ以外の場合は false。

### <a name="method-caption"></a>メソッド caption

テーブルのキャプション プロパティを取得および設定します。

    public str caption()

#### <a name="return-value"></a>戻り値

テーブルのキャプション。

### <a name="method-checkinvalidfieldaccess"></a>メソッド checkInvalidFieldAccess

無効なフィールド アクセスを取得および設定します。

    public boolean checkInvalidFieldAccess([boolean checkInvalidFieldAccess])

#### <a name="parameters"></a>パラメーター

checkInvalidFieldAccess  
設定する値 (オプション)。

#### <a name="return-value"></a>戻り値

無効なフィールド アクセス権が設定されている場合は true。それ以外の場合は、false。

### <a name="method-checkrecord"></a>メソッド checkRecord

必須フィールドをチェックするかどうかを示すプロパティを取得および設定します。

    public boolean checkRecord([boolean checkMandatoryFields])

#### <a name="parameters"></a>パラメーター

checkMandatoryFields  
必須フィールドをチェックするかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

必須項目がオンになっている場合は true。それ以外の場合は、false。

### <a name="method-checkrestricteddeleteactions"></a>メソッド checkRestrictedDeleteActions

レコードが削除されるかどうかを示すプロパティを取得および設定します。

    public boolean checkRestrictedDeleteActions([boolean checkRestrictedDeleteActions])

#### <a name="parameters"></a>パラメーター

checkRestrictedDeleteActions  
レコードが削除できるかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

レコードを削除することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

プロパティはテーブルの削除アクションと、対応するレコードが対応するテーブルにあるときにテーブルが削除アクションを許可するかどうかに基づいています。

### <a name="method-company"></a>メソッド company

レコードの法人を示すプロパティを取得および設定します。

    public SelectableDataArea company([SelectableDataArea company])

#### <a name="parameters"></a>パラメーター

会社  
レコードの新しい法人 (オプション)。

#### <a name="return-value"></a>戻り値

法人 ID。

### <a name="method-con2buf"></a>メソッド con2buf

コンテナをテーブル バッファに展開します。

    public Common con2buf(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

#### <a name="return-value"></a>戻り値

### <a name="method-concurrencymodel"></a>メソッド concurrencyModel

レコードの更新に使用する既定の同時実行モデルを取得および設定します。

    public ConcurrencyModel concurrencyModel([ConcurrencyModel concurrencyModel])

#### <a name="parameters"></a>パラメーター

concurrencyModel  
既定では、新しい同時実行モデル (オプション)。

#### <a name="return-value"></a>戻り値

既定値では、同時実行モデル プロパティの現在の値です。

### <a name="method-context"></a>メソッド context

コンテキスト プロパティを取得および設定します。

    public int context([int newValue])

#### <a name="parameters"></a>パラメーター

newValue  
コンテキスト プロパティの新しい値 (オプション)。

#### <a name="return-value"></a>戻り値

コンテキスト プロパティの現在の値。

### <a name="method-data"></a>メソッド data

テーブルから行を取得します。

    public Common data([Common cursor])

#### <a name="parameters"></a>パラメーター

cursor  
取得する行 (オプション)。

#### <a name="return-value"></a>戻り値

レコード バッファ。

#### <a name="remarks"></a>備考

1 つの理由としてテーブルの継承が関係するシナリオのため、グローバル クラスで con2buf、buf2con、および buf2buf メソッドを代わりに使用することをお勧めします。

### <a name="method-datasource"></a>メソッド dataSource

テーブルのデータ ソースを取得します。

    public FormObjectSet dataSource()

#### <a name="return-value"></a>戻り値

テーブルのデータ ソース。

### <a name="method-disablecache"></a>メソッド disableCache

キャッシュが無効かどうかを示すプロパティを取得および設定します。

    public boolean disableCache([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
キャッシュが無効かどうかを示すブール値。

#### <a name="return-value"></a>戻り値

無効なキャッシュ プロパティの新しい値。

### <a name="method-dovalidatedelete"></a>メソッド doValidateDelete

レコードを削除できる検証するアクションを実行します。

    public boolean doValidateDelete()

#### <a name="return-value"></a>戻り値

### <a name="method-equal"></a>メソッド equal

指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。

    public boolean equal(Common cursor)

#### <a name="parameters"></a>パラメーター

cursor  
等しいかどうかをチェックするオブジェクト。

#### <a name="return-value"></a>戻り値

オブジェクトが等しい場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドは上書きされます。 Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。 派生クラスは、値の等価性をサポートするために Object::equal メソッドを上書きできます。

### <a name="method-fieldaccessright"></a>メソッド fieldAccessRight

フィールドのアクセス権を返します。

    public AccessRight fieldAccessRight(FieldName fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  
フィールド アクセス権を取得するフィールドの名前。

#### <a name="return-value"></a>戻り値

フィールドのフィールド アクセス権限。

### <a name="method-fieldbufferaccessright"></a>メソッド fieldBufferAccessRight

現在のレコードのフィールド アクセス権を返します。

    public AccessRight fieldBufferAccessRight(FieldName fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  
フィールド アクセス権を取得するフィールドの名前。

#### <a name="return-value"></a>戻り値

フィールド アクセス権限。

### <a name="method-fieldstate"></a>メソッド fieldState

テーブル バッファーのフィールドの状態を設定するか返します。

    public FieldState fieldState(FieldId fieldId, [FieldState state])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

状態  

#### <a name="return-value"></a>戻り値

フィールドの古い状態。

### <a name="method-getallowredefault"></a>メソッド getAllowRedefault

既定値に再度設定することを許可されているフィールドの一覧を返します。

    public container getAllowRedefault()

#### <a name="return-value"></a>戻り値

フィールドを保持するコンテナー。

### <a name="method-getdefaultingdependencies"></a>メソッド getDefaultingDependencies

デフォルトの依存関係を保持するコンテナーを返します。

    public container getDefaultingDependencies()

#### <a name="return-value"></a>戻り値

デフォルトの依存関係を保持するコンテナー。

### <a name="method-getextension"></a>メソッド getExtension

テーブル拡張機能を返します。

    public TableExtension getExtension()

#### <a name="return-value"></a>戻り値

テーブル拡張

### <a name="method-getfieldvalue"></a>メソッド getFieldValue

テーブル バッファから指定したフィールドの値を取得します。

    public AnyType getFieldValue(str fieldName, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldName  
フィールドの配列インデックス (省略可能)。

<!-- -->

arrayIndex  
フィールドの配列インデックス (省略可能)。

#### <a name="return-value"></a>戻り値

フィールドの値。

#### <a name="remarks"></a>備考

arrayIndex パラメーターは、配列フィールドにのみ適用されます。 配列でないフィールドには、このパラメーターを省略するか、または 0 (ゼロ) を指定します。 指定されたフィールドが不明な場合、このメソッドは ArgumentOutOfRange 例外をスローします。

### <a name="method-getinstancerelationtype"></a>メソッド getInstanceRelationType

InstanceRelationType ID に対応するテーブルの名前を返します。

    public str getInstanceRelationType()

#### <a name="return-value"></a>戻り値

InstanceRelationType ID に対応するテーブルの名前。

### <a name="method-getphysicaltablename"></a>メソッド getPhysicalTableName

物理テーブル名を返します。SQL Temp DB テーブルの場合は、テーブル インスタンス名です。

    public str getPhysicalTableName()

#### <a name="return-value"></a>戻り値

物理テーブル名またはテーブル インスタンス名。

### <a name="method-getpresencefielddata"></a>メソッド getPresenceFieldData

指定されたフィールドから PresenceInfo 値を取得します。

    public PresenceInfo getPresenceFieldData(FieldId fieldId, AnyType fieldValue)

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

fieldValue  

#### <a name="return-value"></a>戻り値

### <a name="method-getsqlstatement"></a>メソッド getSQLStatement

レコードをデータベースから取得するために使用される SQL ステートメントを取得します。

    public str getSQLStatement()

#### <a name="return-value"></a>戻り値

SQL ステートメントを含む文字列。

### <a name="method-gettableininstancehierarchy"></a>メソッド getTableInInstanceHierarchy

    public Common getTableInInstanceHierarchy(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

#### <a name="return-value"></a>戻り値

### <a name="method-gettabletype"></a>メソッド getTableType

テーブルのタイプを示します。

    public TableType getTableType()

#### <a name="return-value"></a>戻り値

テーブルのタイプ (Regular、InMemory、TempDB)。

### <a name="method-hasrelatedtable"></a>メソッド hasRelatedTable

外部キー制約バッファがテーブルにリンクされているかどうかを示します。

    public boolean hasRelatedTable(str relatedRoleName)

#### <a name="parameters"></a>パラメーター

relatedRoleName  

#### <a name="return-value"></a>戻り値

外部キー制約バッファがテーブルにリンクされている場合は true。それ以外の場合は、false。

### <a name="method-helpfield"></a>メソッド helpField

指定したフィールドのヘルプ テキストを含む文字列を取得します。

    public str helpField(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  
ヘルプ テキストを取得するフィールド。

#### <a name="return-value"></a>戻り値

指定されたフィールドのヘルプ文字列。

### <a name="method-inputstatus"></a>メソッド inputStatus

テーブル バッファーの現在の入力ステータスを設定するか返します。

    public FieldState inputStatus([FieldState inputStatus])

#### <a name="parameters"></a>パラメーター

inputStatus  

#### <a name="return-value"></a>戻り値

古い入力のステータス。

### <a name="method-interactivecontext"></a>メソッド interactiveContext

テーブル バッファーの現在のインタラクティブ コンテキストを設定するか返します。

    public boolean interactiveContext([boolean context])

#### <a name="parameters"></a>パラメーター

context  

#### <a name="return-value"></a>戻り値

テーブル バッファーの現在の対話型コンテキスト。

### <a name="method-isfielddataretrieved"></a>メソッド isFieldDataRetrieved

指定されたフィールドのデータが取得されたかどうかをチェックします。

    public boolean isFieldDataRetrieved(str fieldName, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

データが取得済みの場合は true。それ以外の場合は、false。

### <a name="method-isfieldset"></a>メソッド isFieldSet

フィールドがセットまたは既定状態かどうかをチェックします。

    public boolean isFieldSet(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  

#### <a name="return-value"></a>戻り値

フィールドがセット状態または既定状態の場合は true。それ以外の場合は、false。

### <a name="method-isformdatasource"></a>メソッド isFormDataSource

データ ソースがフォームであるかどうかを示します。

    public boolean isFormDataSource()

#### <a name="return-value"></a>戻り値

データ ソースがフォームである場合は true。それ以外の場合は、false。

### <a name="method-isnewrecord"></a>メソッド isNewRecord

レコードがまだ保存されていない新しいレコードである場合は true を返します。

    public boolean isNewRecord()

#### <a name="return-value"></a>戻り値

レコードがまだ保存されていない新しいレコードである場合は true。それ以外の場合は、false。

### <a name="method-ispartofuowsavechanges"></a>メソッド isPartOfUOWSaveChanges

    public boolean isPartOfUOWSaveChanges()

#### <a name="return-value"></a>戻り値

### <a name="method-istempdb"></a>メソッド isTempDb

テーブルのタイプが SQL TempDB であるかどうかを示します。

    public boolean isTempDb()

#### <a name="return-value"></a>戻り値

テーブルのタイプが SQL TempDB である場合は true。それ以外の場合は false。

### <a name="method-istmp"></a>メソッド isTmp

これが一時テーブルであるかどうかを示します。

    public boolean isTmp()

#### <a name="return-value"></a>戻り値

これが一時テーブルである場合は true。それ以外の場合は false。

### <a name="method-joinchild"></a>メソッド joinChild

現在のレコードの結合子を検索します。

    public Common joinChild()

#### <a name="return-value"></a>戻り値

現在のレコードの結合子。

### <a name="method-joinparent"></a>メソッド joinParent

現在のレコードの結合の親を検索します。

    public Common joinParent()

#### <a name="return-value"></a>戻り値

現在のレコードの結合の親。

### <a name="method-linkphysicaltableinstance"></a>メソッド linkPhysicalTableInstance

レコードの物理テーブル インスタンスへのリンクがあるかどうかを確認します。

    public boolean linkPhysicalTableInstance([Common record])

#### <a name="parameters"></a>パラメーター

記録  

#### <a name="return-value"></a>戻り値

リンク使用可能かどうかを示すブール値。

### <a name="method-orig"></a>メソッド orig

現在のレコードの元の値を取得します。

    public Common orig()

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

1 つの理由としてテーブルの継承が関係するシナリオのため、グローバル クラスで con2buf、buf2con、および buf2buf メソッドを代わりに使用することをお勧めします。

### <a name="method-overwritesystemfields"></a>メソッド overwriteSystemfields

システム フィールドを上書きできるかどうかを示すプロパティを取得および設定します。

    public boolean overwriteSystemfields([boolean allowOverwrite])

#### <a name="parameters"></a>パラメーター

allowOverwrite  
システム フィールドを上書きできるかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

システム フィールドを上書きすることができる場合は true。それ以外の場合は、false。

### <a name="method-querytimedout"></a>メソッド queryTimedOut

クエリが実行の時間制限を超過したかどうかを示します。

    public boolean queryTimedOut()

#### <a name="return-value"></a>戻り値

クエリが実行の時間制限を超過した場合は true。それ以外の場合は、false。

### <a name="method-querytimeout"></a>メソッド queryTimeout

クエリの実行に対する時間制限を示すプロパティを取得および設定します。

    public int queryTimeout([int seconds], [boolean raiseException])

#### <a name="parameters"></a>パラメーター

 秒  

<!-- -->

raiseException  

#### <a name="return-value"></a>戻り値

クエリ タイムアウト プロパティの現在の値。

### <a name="method-readcommittedlock"></a>メソッド readCommittedLock

    public boolean readCommittedLock([boolean readCommittedLock])

#### <a name="parameters"></a>パラメーター

readCommittedLock  

#### <a name="return-value"></a>戻り値

### <a name="method-readpast"></a>メソッド readPast

レコードの読み取り時に、他のプロセスによりロックされる行をスキップするかどうかを示すプロパティを取得および設定します。

    public boolean readPast([boolean skipLockedRows])

#### <a name="parameters"></a>パラメーター

skipLockedRows  
ロックされている行をスキップするかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

ロックされた行をスキップする必要がある場合は true。それ以外の場合は、false。

### <a name="method-recordlevelsecurity"></a>メソッド recordLevelSecurity

レコード レベルのセキュリティを適用するかどうかを示すプロパティを取得および設定します。

    public boolean recordLevelSecurity([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
レコード レベルのセキュリティを適用するかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

セキュリティをレコード レベルで適用する必要がある場合は true。それ以外の場合は、false。

### <a name="method-relatedtable"></a>メソッド relatedTable

テーブル バッファのリンクに関連するバッファーを設定するか返します。

    public Common relatedTable(str name, [Common buffer])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

バッファ  

#### <a name="return-value"></a>戻り値

テーブル バッファのリンクに関連するバッファ。

### <a name="method-rowcount"></a>メソッド RowCount

テーブル内の行数を取得します。

    public Int64 RowCount()

#### <a name="return-value"></a>戻り値

テーブルの行数。

### <a name="method-selectforupdate"></a>メソッド selectForUpdate

読み取り時に更新用のレコードを選択するかどうかを示すプロパティを取得および設定します。

    public boolean selectForUpdate([boolean lockRecordsExclusive])

#### <a name="parameters"></a>パラメーター

lockRecordsExclusive  
更新のためにレコードを読み込むかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

更新のためにレコードを読み取る必要がある場合は true。それ以外の場合は、false。

### <a name="method-selectlocked"></a>メソッド selectLocked

ロックされているレコードを選択するかどうかを示します。

    public boolean selectLocked([boolean lockRecordsShared])

#### <a name="parameters"></a>パラメーター

lockRecordsShared  
ロックされているレコードを選択するかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

ロックされたレコードを選択する必要がある場合は true。それ以外の場合は、false。

### <a name="method-selectrefrecord"></a>メソッド selectRefRecord

参照されているフィールド ID によりレコードを選択します。

    public Common selectRefRecord(FieldId referenceFieldId)

#### <a name="parameters"></a>パラメーター

referenceFieldId  
参照フィールド ID。

#### <a name="return-value"></a>戻り値

レコード バッファ。

### <a name="method-selectwithrepeatableread"></a>メソッド selectWithRepeatableRead

反復可能な読み取りが有効かどうかを示すプロパティを取得および設定します。

    public boolean selectWithRepeatableRead([boolean useRepeatableRead])

#### <a name="parameters"></a>パラメーター

useRepeatableRead  
反復可能な読み取りが有効かどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

反復可能な読み取りが有効な場合は true。それ以外の場合は、false。

### <a name="method-settempdb"></a>メソッド setTempDB

    public boolean setTempDB()

#### <a name="return-value"></a>戻り値

### <a name="method-settmp"></a>メソッド setTmp

データベースに保存されていない場合にテーブルを設定します。

    public boolean setTmp()

#### <a name="return-value"></a>戻り値

操作が成功した場合は true。それ以外の場合は、false。

### <a name="method-skipaosvalidation"></a>メソッド skipAosValidation

Finance and Operations Application Object Server (AOS) の検証をスキップするかどうかを示すプロパティを取得および設定します。

    public boolean skipAosValidation([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
AOS の検証をスキップするかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

AOS 検証をスキップする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

攻撃者が skipAosValidation メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、SkipAOSValidationPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発ユーザー権を持っていることを確認します。

### <a name="method-skipdatabaselog"></a>メソッド skipDatabaseLog

データベース ログ要求をスキップするかどうかを示すプロパティを取得および設定します。

    public boolean skipDatabaseLog([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
データベース ログ要求をスキップするかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

データベース ログ要求をスキップする必要がある場合は true。それ以外の場合は、false。

### <a name="method-skipdatamethods"></a>メソッド skipDataMethods

オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。

    public boolean skipDataMethods([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
オーバーロードされたメソッドを破棄するかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

オーバーロードされたメソッドを破棄する必要がある場合は true。それ以外の場合は、false。

### <a name="method-skipdeleteactions"></a>メソッド skipDeleteActions

テーブルで削除アクションをスキップするかどうかを示すプロパティを取得および設定します。

    public boolean skipDeleteActions([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
レコードの削除要求を無視するかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

レコードを削除する要求を無視する必要がある場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドは、delete\_from ステートメントなど、セットベースの操作を使用している場合にのみ機能します。 xRecord.delete メソッドなどの行ベースの操作でそれを使用する場合、プロパティは重視されず、削除アクションは引き続き呼び出されます。

### <a name="method-skipdeletemethod"></a>メソッド skipDeleteMethod

オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。

    public boolean skipDeleteMethod([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
オーバーロードされたメソッドを破棄するかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

オーバーロードされたメソッドを破棄する必要がある場合は true。それ以外の場合は、false。

### <a name="method-skipevents"></a>メソッド skipEvents

xRecord オブジェクトの有効期間の Application.event\* メソッドの呼び出しをオフにするオプションを提供します。

    public boolean skipEvents([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
イベントをスキップするかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

イベントがスキップされる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドは、xRecord.skipDatabaseLog メソッドに似ています。 skipEvents メソッドは、カーネル内で生成するのに意味のないイベントをスキップするためにも内部的に使用されます。これは xRecord.skipDatabaseLog メソッドの現在の動作と一致しています。

-   Application.deleteCompany メソッド: 会社の削除操作の期間にイベント生成が無効になります。 これは管理操作であり、この場合はイベントをサポートするためのパフォーマンス上の問題が発生する可能性があります。
-   SqlDataDictionary.tableDelete メソッド: テーブル削除時にイベント生成がオフになります。 これは管理操作であり、この場合はイベントをサポートするためのパフォーマンス上の問題が発生する可能性があります。
-   カーネルで配列挿入機能を実装する RecordInsertList クラスは、開発者によって指定されたイベントを条件付きでスキップする新しいメソッドで、オプション引数 \_skipEvents = false を取得します。 イベントがスキップされない場合でも、カーネルは SQL を書き換えません。
-   主キーの名前を変更するとき、名前の変更操作が終了するまで、イベントの生成が停止されます。 これには、1 つのレコード内の主キーが含まれ、多くのレコードに外部キーを含まれることができます。 リネーム操作後、eventRenameKey メソッドが呼び出されます。

### <a name="method-skippostload"></a>メソッド skipPostLoad

テーブルで xRecord.postLoad メソッドの実行をスキップするかどうかを示すプロパティを取得および設定します。

    public boolean skipPostLoad([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
テーブルの postLoad メソッドの実行をスキップするかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

postLoad メソッドの実行をスキップする場合は true。それ以外の場合は、false。

### <a name="method-skipttscheck"></a>メソッド skipTTSCheck

更新用にレコードが選択されているかどうかを決定するため、チェックをスキップするかどうかを示すプロパティを取得および設定します。

    public boolean skipTTSCheck([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
チェックをスキップするかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

TTS チェックをスキップする必要がある場合は true。それ以外の場合は false。

### <a name="method-suppresswarnings"></a>メソッド suppressWarnings

このポインタの警告を非表示にするかどうかを示すプロパティを取得および設定します。

    public boolean suppressWarnings([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  
このポインタの警告を非表示にするかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

このポインターの警告を抑制する必要がある場合は true。それ以外の場合は、false。

### <a name="method-tableaccessright"></a>メソッド tableAccessRight

テーブルのアクセス権を返します。

    public AccessRight tableAccessRight()

#### <a name="return-value"></a>戻り値

テーブル アクセス権の値。

### <a name="method-tablebufferaccessright"></a>メソッド tableBufferAccessRight

現在のレコードのテーブル アクセス権を返します。

    public AccessRight tableBufferAccessRight()

#### <a name="return-value"></a>戻り値

現在のレコードのテーブル アクセス権。

### <a name="method-takeownershipoftempdbtable"></a>メソッド takeOwnershipOfTempDBTable

    public boolean takeOwnershipOfTempDBTable(boolean newValue)

#### <a name="parameters"></a>パラメーター

newValue  

#### <a name="return-value"></a>戻り値

### <a name="method-tooltipfield"></a>メソッド toolTipField

指定されたフィールドの HelpText 値を取得します。

    public str toolTipField(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  
HelpText の値を取得するフィールド。

#### <a name="return-value"></a>戻り値

指定されたフィールドの HelpText 値。

### <a name="method-tooltiprecord"></a>メソッド toolTipRecord

現在のレコードのツールヒント値を取得します。

    public str toolTipRecord()

#### <a name="return-value"></a>戻り値

現在のレコードのツールヒント値。

### <a name="method-usagecount"></a>メソッド usageCount

オブジェクトが持つ参照 (参照カウンターの値) の現在の番号を取得します。

    public int usageCount()

#### <a name="return-value"></a>戻り値

オブジェクトが持つ参照の現在の数。

#### <a name="remarks"></a>備考

このメソッドは上書きされます。 オブジェクトが作成されると、その参照カウンターが 1 になります。 新しい参照が作成されると、その値が増加します。 スコープ外の参照は、値が減少します。

### <a name="method-useexistingtempdbtable"></a>メソッド useExistingTempDBTable

    public boolean useExistingTempDBTable(str physicalTempTableName)

#### <a name="parameters"></a>パラメーター

physicalTempTableName  

#### <a name="return-value"></a>戻り値

### <a name="method-validatedelete"></a>メソッド validateDelete

現在のレコードが有効で、データベースから削除する準備ができているかどうかを調べます。

    public boolean validateDelete()

#### <a name="return-value"></a>戻り値

現在のレコードを削除することができる場合は true。それ以外の場合は、false。

### <a name="method-validatefield"></a>メソッド validateField

指定されたフィールドが有効かどうかを判定します。

    public boolean validateField(FieldId fieldIdToCheck)

#### <a name="parameters"></a>パラメーター

fieldIdToCheck  
検証対象のフィールドのフィールド ID です。

#### <a name="return-value"></a>戻り値

指定したフィールドが有効である場合は true。それ以外の場合は false。

### <a name="method-validatefieldvalue"></a>メソッド validateFieldValue

    public boolean validateFieldValue(FieldName fieldName, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-validaterelations"></a>メソッド validateRelations

    private container validateRelations([boolean onlyValidateCompositeRelations], [boolean onlyValidateModifiedRelations])

#### <a name="parameters"></a>パラメーター

onlyValidateCompositeRelations  

<!-- -->

onlyValidateModifiedRelations  

#### <a name="return-value"></a>戻り値

### <a name="method-validatewrite"></a>メソッド validateWrite

現在のレコードが有効で、書き込み可能な状態かどうかを判別します。

    public boolean validateWrite()

#### <a name="return-value"></a>戻り値

現在のレコードを記述することができる場合は true。それ以外の場合は、false。

### <a name="method-validtimestateupdatemode"></a>メソッド validTimeStateUpdateMode

カーソルで有効な時間状態更新モードを設定します。

    public ValidTimeStateUpdate validTimeStateUpdateMode(ValidTimeStateUpdate validTimeStateUpdateMode)

#### <a name="parameters"></a>パラメーター

validTimeStateUpdateMode  

#### <a name="return-value"></a>戻り値

有効時間状態の更新モードの古い値。

### <a name="method-wascached"></a>メソッド wasCached

データの取得元となった場所を指定します。

    public CachedHow wasCached()

#### <a name="return-value"></a>戻り値

データが取得された場所を示す CachedHow 列挙値。

### <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を取得します。

    public str xml([int indent])

#### <a name="parameters"></a>パラメーター

インデント  
XML 文字列のインデントに使用するスペースの数を示す整数。

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す XML 文字列です。

#### <a name="remarks"></a>備考

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

### <a name="method-dodelete"></a>メソッド doDelete

現在のレコードをテーブルから削除し、テーブルの delete メソッドの追加ロジックをバイパスします。

    public void doDelete()

### <a name="method-update"></a>メソッド update

現在のレコードを更新します。

    public void update()

### <a name="method-merge"></a>メソッド merge

現在のテーブルを指定されたテーブルとマージします。

    public void merge(Common mergeInto)

#### <a name="parameters"></a>パラメーター

mergeInto  
マージするテーブル。

### <a name="method-clear"></a>メソッド clear

テーブル バッファーからすべての行を削除します。

    public void clear()

### <a name="method-setxdscontext"></a>メソッド setXDSContext

新しい XDS コンテキストを設定します。

    public void setXDSContext([str contextString])

#### <a name="parameters"></a>パラメーター

contextString  

### <a name="method-renameprimarykey"></a>メソッド renamePrimaryKey

この表の対応する主キーの値の変更に従って、他のテーブルの外部キーの名前を変更します。

    public void renamePrimaryKey()

### <a name="method-dispose"></a>メソッド dispose

XRecord オブジェクトによって使用されているリソースを解放します。

    public void dispose()

### <a name="method-setconnection"></a>メソッド setConnection

この表のユーザー接続を設定します。

    public void setConnection(Connection connection)

#### <a name="parameters"></a>パラメーター

connection  

### <a name="method-delete"></a>メソッド delete

テーブルから現在のレコードを削除します。

    public void delete()

### <a name="method-defaultfield"></a>メソッド defaultField

テーブルのフィールドの既定値を設定します。

    public void defaultField(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  

### <a name="method-dbopintransaction"></a>メソッド dbOpInTransaction

失敗した場合にデータベース操作が正しく閉じられていることを確認します。

    private void dbOpInTransaction([boolean isWriteOperation])

#### <a name="parameters"></a>パラメーター

isWriteOperation  
操作が書き込み操作かどうかを示すブール値; オプション。

### <a name="method-write"></a>メソッド write

レコードが存在する場合は更新します。存在しない場合はレコードを挿入します。

    public void write()

### <a name="method-preremoting"></a>メソッド preRemoting

他のレベルに状態をパックしているテーブルに対してレベル間の呼び出しが実行される前に実行されます。

    public void preRemoting()

### <a name="method-modifiedfieldvalue"></a>メソッド modifiedFieldValue

指定したフィールドを元の値に変更します。

    public void modifiedFieldValue(FieldName fieldName, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldName  
フィールドの配列インデックス (省略可能)。

<!-- -->

arrayIndex  
フィールドの配列インデックス (省略可能)。

### <a name="method-defaultrow"></a>メソッド defaultRow

非対話型の場合、テーブルのフィールドの既定値を設定します。

    public void defaultRow()

### <a name="method-reread"></a>メソッド reread

テーブルからレコードを再読み取りします。

    public void reread()

### <a name="method-modifiedfield"></a>メソッド modifiedField

指定したフィールドを元通りに変更します。

    public void modifiedField(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  
変更対象のフィールド ID。

### <a name="method-ttsabort"></a>メソッド ttsabort

ttsbegin メソッドの呼び出しによって開始されたトランザクションの廃棄。

    public void ttsabort()

### <a name="method-insert"></a>メソッド insert

テーブルにレコードを挿入します。

    public void insert()

### <a name="method-doclear"></a>メソッド doClear

現在の行をテーブル バッファーから削除し、テーブルの clear メソッドの追加ロジックをバイパスします。

    public void doClear()

### <a name="method-initvalue"></a>メソッド initValue

フィールドを既定値に初期化します。

    public void initValue()

### <a name="method-doupdate"></a>メソッド doUpdate

現在のレコードを更新し、テーブルの更新メソッドにある追加ロジックをバイパスします。

    public void doUpdate()

### <a name="method-ttsbegin"></a>メソッド ttsbegin

ttscommit メソッドによりコミット、または ttsabort メソッドによって中止できるトランザクションを開始します。

    public void ttsbegin()

### <a name="method-setcrosspartition"></a>メソッド setCrossPartition

テーブルのパーティション間分割を設定またはリセットします。

    public void setCrossPartition(boolean newValue)

#### <a name="parameters"></a>パラメーター

newValue  
クロス パーティションをセットまたはリセットする新しいブール値。

### <a name="method-settmpdata"></a>メソッド setTmpData

一時的なテーブルの内容を指定されたデータに設定します。

    public void setTmpData(Common cursor)

#### <a name="parameters"></a>パラメーター

cursor  
一時テーブルの新しいデータ。

### <a name="method-ttscommit"></a>メソッド ttscommit

ttsbegin メソッドの呼び出しによって開始されたトランザクションをコミットします。

    public void ttscommit()

### <a name="method-setfieldvalue"></a>メソッド setFieldValue

レコード バッファーのフィールド値を設定します。

    public void setFieldValue(str fieldName, AnyType value, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldName  
フィールドの配列インデックス (省略可能)。

<!-- -->

値  
フィールドの配列インデックス (省略可能)。

<!-- -->

arrayIndex  
フィールドの配列インデックス (省略可能)。

#### <a name="remarks"></a>備考

arrayIndex パラメーターは、配列フィールドにのみ適用されます。 配列でないフィールドには、このパラメーターを省略するか、または 0 (ゼロ) を指定します。 このメソッドは、指定されたフィールドが不明な場合は ArgumentOutOfRange 例外をスローし、値パラメーターが指定されたフィールドと互換性がない場合は TypeMismatch 例外をスローします。

### <a name="method-doinsert"></a>メソッド doInsert

テーブルにレコードを挿入し、テーブルの挿入メソッドで追加のロジックをバイパスします。

    public void doInsert()

### <a name="method-setsqltracing"></a>メソッド setSQLTracing

SQL トレース モードを有効または無効にします。

    public void setSQLTracing([boolean tracingmode])

#### <a name="parameters"></a>パラメーター

tracingmode  

### <a name="method-postload"></a>メソッド postLoad

レコードが読み取られた後に実行されます。

    public void postLoad()

## <a name="class-xref"></a>クラス xRef
    class xRef extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明                                     |
|------------------------------------------------|-------------------------------------------------|
| public AccessLevel accessLevel()               |                                                 |
| public int column()                            |                                                 |
| public container contents()                    |                                                 |
| public xRefKind kind()                         |                                                 |
| public int line()                              |                                                 |
| public XRefMode mode()                         |                                                 |
| public str name()                              |                                                 |
| public str path()                              |                                                 |
| public XRefReference reference()               |                                                 |
| public int typeHandle()                        |                                                 |
| public str typeName(xRefKind kind, int handle) |                                                 |
| public void new(container data)                | Object クラスの新しいインスタンスを初期化します。 |
| public void init()                             |                                                 |
| public void finalize()                         |                                                 |
| public void next()                             |                                                 |

### <a name="method-accesslevel"></a>メソッド accessLevel

    public AccessLevel accessLevel()

#### <a name="return-value"></a>戻り値

### <a name="method-column"></a>メソッド column

    public int column()

#### <a name="return-value"></a>戻り値

### <a name="method-contents"></a>メソッド contents

    public container contents()

#### <a name="return-value"></a>戻り値

### <a name="method-kind"></a>メソッド kind

    public xRefKind kind()

#### <a name="return-value"></a>戻り値

### <a name="method-line"></a>メソッド line

    public int line()

#### <a name="return-value"></a>戻り値

### <a name="method-mode"></a>メソッド mode

    public XRefMode mode()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-path"></a>メソッド path

    public str path()

#### <a name="return-value"></a>戻り値

### <a name="method-reference"></a>メソッド reference

    public XRefReference reference()

#### <a name="return-value"></a>戻り値

### <a name="method-typehandle"></a>メソッド typeHandle

    public int typeHandle()

#### <a name="return-value"></a>戻り値

### <a name="method-typename"></a>メソッド typeName

    public str typeName(xRefKind kind, int handle)

#### <a name="parameters"></a>パラメーター

kind  

<!-- -->

handle  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(container data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-init"></a>メソッド init

    public void init()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-next"></a>メソッド next

    public void next()

## <a name="class-xresourcenode"></a>クラス xResourceNode
    class xResourceNode extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                   | 説明 |
|--------------------------------------------------------------------------|-------------|
| public BinData AOTGetData()                                              |             |
| public Image AOTGetImage()                                               |             |
| public str changedBy(\[str value\])                                      |             |
| public Date changedDate(\[Date value\])                                  |             |
| public str changedTime(\[str value\])                                    |             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\]) |             |
| public str createdBy(\[str value\])                                      |             |
| public Date creationDate(\[Date value\])                                 |             |
| public str creationTime(\[str value\])                                   |             |
| public str filename(\[str value\])                                       |             |
| public str helpText(\[str value\])                                       |             |
| public str label(\[str value\])                                          |             |
| public str name(\[str value\])                                           |             |
| public Guid origin(\[Guid value\])                                       |             |
| ::public static Image AOTCreateImage(str imageName)                      |             |
| public void AOTSetData(BinData data)                                     |             |
| public void AOTSetImage(Image image)                                     |             |

### <a name="method-aotgetdata"></a>メソッド AOTGetData

    public BinData AOTGetData()

#### <a name="return-value"></a>戻り値

### <a name="method-aotgetimage"></a>メソッド AOTGetImage

    public Image AOTGetImage()

#### <a name="return-value"></a>戻り値

### <a name="method-changedby"></a>メソッド changedBy

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-changeddate"></a>メソッド changedDate

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-changedtime"></a>メソッド changedTime

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-createdby"></a>メソッド createdBy

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-creationdate"></a>メソッド creationDate

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-filename"></a>メソッド filename

    public str filename([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aotcreateimage"></a>メソッド AOTCreateImage

    public static Image AOTCreateImage(str imageName)

#### <a name="parameters"></a>パラメーター

imageName  

#### <a name="return-value"></a>戻り値

### <a name="method-aotsetdata"></a>メソッド AOTSetData

    public void AOTSetData(BinData data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-aotsetimage"></a>メソッド AOTSetImage

    public void AOTSetImage(Image image)

#### <a name="parameters"></a>パラメーター

image  

## <a name="class-xsession"></a>クラス xSession
    class xSession extends Object

Finance and Operations セッションに関する情報を取得します。

### <a name="remarks"></a>備考

現在のセッションに関する情報を取得するには、パラメーターを指定せずに新しい xSession セッションを作成します。 すべてのアクティブなセッション (AOS のみ) に関する情報を取得する唯一の方法は、セッション ID 1 から xSession.maxSessionId に移動することです。 ID は、永続的な一覧ではなく、maxSessionId メソッドで指定したセッションの最大数を超えることはありません。

### <a name="examples"></a>例

次の例では、新しい xSession オブジェクトを作成し、それを使用して現在のセッションのサーバー名を検索します。

    xSession xSession; 
    xSession = new xSession();   
    // Prints the name of server for the current session. 
    print xSession.AOSName();

### <a name="methods"></a>メソッド

| 方法                                                                            | 説明                                                                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| public str AOSName()                                                              | セッションの処理を担当する Application Object Server (AOS) の名前を取得します。                       |
| public str clientComputerName()                                                   | セッションの処理を担当するクライアント コンピューターのネットワーク名を取得します。                               |
| public ClientType clientKind()                                                    | セッションの処理を担当するクライアントの種類を取得します。                                                |
| public str databaseSpid()                                                         | 有効な接続 ID のコンマ区切りのリストを取得します。                                                                     |
| public str documentationLanguage()                                                | セッションに表示されるドキュメントの言語 ID を取得します。                                                  |
| public str interfaceLanguage()                                                    | セッションのメニューとダイアログで使用される言語の ID を取得します。                                           |
| public boolean isWorkerThread()                                                   | セッションがワーカー スレッドかどうかを判定します。                                                                             |
| public Date loginDate()                                                           | セッションのユーザーがログオンした日付を取得します。                                                                 |
| public DateTime loginDateTime()                                                   |                                                                                                                                |
| public TimeOfDay loginTime()                                                      | セッションのユーザーがログオンした時刻を取得します。                                                                 |
| public int masterSessionId()                                                      | xSession オブジェクトの対象となるセッションのマスター セッション ID を取得します。                                               |
| public int serverId()                                                             |                                                                                                                                |
| public int sessionId()                                                            | xSession オブジェクトの対象となるセッションのセッション ID を取得します。                                                       |
| public boolean terminate(\[Date loginDate\], \[TimeOfDay loginTime\])             | オブジェクトのインスタンス化に使用されたセッション ID を終了します。                                                               |
| public UserId userId()                                                            | このセッションがログオンしているユーザー ID を取得します。                                                                     |
| ::public static int currentRetryCount()                                           | デッドロック、更新の競合、または別の例外の後に try ブロックが再試行された回数をカウントします。            |
| ::public static Uncheck currentUnCheck()                                          |                                                                                                                                |
| ::public static str getDbSchema()                                                 | セッションのデータベース オブジェクト名のスキーマ部分を取得します。                                                         |
| ::public static COM getIISObject(IISObject object)                                | IIS オブジェクトの COM オブジェクトのインスタンスを作成して返します。                                                                       |
| ::public static boolean getSysTraceActive()                                       | セッションでシステム トレースを有効にするかどうかを決定できます。                                                  |
| ::public static str getXRefAssembyTempFolder()                                    |                                                                                                                                |
| ::public static boolean isCLRSession()                                            |                                                                                                                                |
| ::public static boolean isUserPreferredTzSameAsLocalMachine()                     |                                                                                                                                |
| ::public static int lastDuplicateKeyViolatingTable()                              |                                                                                                                                |
| ::public static int lastUpdateConflictingTable()                                  | 最後に更新の競合をしたテーブルのインスタンスを取得します。                                                  |
| ::public static int maxSessionId()                                                | 現在のライセンス コードで許可されているセッションの最大数を取得します。                                      |
| ::public static int numSession()                                                  | 登録されているセッションの現在の番号を取得します。                                                                           |
| public PreferredLocale preferredLocale()                                          |                                                                                                                                |
| ::public static int pseudoBandwidth(\[int bandwidth\])                            | セッションの帯域幅シミュレーションをオンにするかどうかを決定し、帯域幅シミュレーションをオンまたはオフにします。 |
| ::public static int pseudoLatency(\[int latency\])                                | セッションの待機シミュレーションをオンにするかどうかを決定し、待機シミュレーションをオンまたはオフにします。     |
| ::public static int pseudoSimMode(\[int simMode\])                                | セッションの遅延シミュレーションをオンにするかどうかを決定し、遅延シミュレーションをオンまたはオフにします。         |
| ::public static int systemSessionId()                                             | xSession オブジェクトの対象となるセッションのシステム セッション ID を取得します。                                               |
| ::public static container xppCallStack()                                          | 現在の呼び出し履歴を取得します。                                                                                              |
| ::public static void removeAOC()                                                  | 現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を削除します。                                         |
| ::public static void updateAOC()                                                  | 現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を更新します。                                         |
| ::public static void setAutoUpdateRecVersion(boolean autoUpdateRecVersion)        |                                                                                                                                |
| ::public static void setSysTraceActive(boolean nValue)                            | システム追跡のオンまたはオフを切り替えます。                                                                                             |
| ::private static void clientSetAutoUpdateRecVersion(boolean autoUpdateRecVersion) |                                                                                                                                |
| ::private static void serverSetAutoUpdateRecVersion(boolean autoUpdateRecVersion) |                                                                                                                                |
| public void new(\[int sessionId\], \[boolean checkSession\])                      | 現在のセッションまたはパラメーターとして渡されたセッション ID のいずれかに対して xSession オブジェクトのインスタンスを作成します。                   |
| ::public static void reloadTableCollectionOnClient()                              |                                                                                                                                |

### <a name="method-aosname"></a>メソッド AOSName

セッションの処理を担当する Application Object Server (AOS) の名前を取得します。

    public str AOSName()

#### <a name="return-value"></a>戻り値

AOS の名前を示す文字列。

#### <a name="remarks"></a>備考

AOS以外の接続されているクライアントについては、このメソッドは、空の文字列を返します。

#### <a name="examples"></a>例

次の例は、現在のセッションを実行している AOS の名前を表示します。

    xSession xSession; 
    xSession = new xSession(); 
    // Prints the name of server for the current session. 
    print xSession.AOSName();

### <a name="method-clientcomputername"></a>メソッド clientComputerName

セッションの処理を担当するクライアント コンピューターのネットワーク名を取得します。

    public str clientComputerName()

#### <a name="return-value"></a>戻り値

クライアント コンピューターの名前を示す文字列。

#### <a name="examples"></a>例

次の例は、現在のセッションを実行しているクライアントの名前を表示します。

    { 
        xSession xSession; 
        xSession = new xSession(); 
        print xSession.clientComputerName(); 
        pause; 
    }

### <a name="method-clientkind"></a>メソッド clientKind

セッションの処理を担当するクライアントの種類を取得します。

    public ClientType clientKind()

#### <a name="return-value"></a>戻り値

クライアントのタイプ。

#### <a name="remarks"></a>備考

可能な値は、ClientType システム列挙の値です。

-   COMObject
-   クライアント
-   サーバー
-   WorkerThread

#### <a name="examples"></a>例

次の例は、現在のセッションを実行しているクライアントのタイプを表示します。

    { 
        xSession xSession; 
        xSession = new xSession(); 
        print xSession.clientKind(); 
        pause; 
    }

### <a name="method-databasespid"></a>メソッド databaseSpid

有効な接続 ID のコンマ区切りのリストを取得します。

    public str databaseSpid()

#### <a name="return-value"></a>戻り値

有効な接続 ID のコンマ区切りのリスト。

#### <a name="remarks"></a>備考

このメソッドは、オンライン ユーザー フォーム (SysUsersOnline) を作成するために使用されます。 有効な接続の数を取得するには、xSession::numSession を使用します。

### <a name="method-documentationlanguage"></a>メソッド documentationLanguage

セッションに表示されるドキュメントの言語 ID を取得します。

    public str documentationLanguage()

#### <a name="return-value"></a>戻り値

セッションのドキュメントに使用される言語の ID を含む文字列。

#### <a name="remarks"></a>備考

たとえば、このメソッドは、言語が英語 (US) に設定されている場合「en-us」を返します。 ドキュメントの言語は個別に選択することができ、メニューやダイアログで使用される言語と必ずしも同一ではありません。 メニューやダイアログ ボックスの言語 ID を取得するには、xSession.interfaceLanguage を使用します。 xInfo.documentationLanguage を使用すると、ドキュメントの言語を設定することができます。

### <a name="method-interfacelanguage"></a>メソッド interfaceLanguage

セッションのメニューとダイアログで使用される言語の ID を取得します。

    public str interfaceLanguage()

#### <a name="return-value"></a>戻り値

セッションのメニューとダイアログで使用される言語の ID を含む文字列。

#### <a name="remarks"></a>備考

たとえば、このメソッドは、言語が英語 (US) に設定されている場合「en-us」を返します。 ドキュメントの言語は個別に選択することができ、メニューやダイアログで使用される言語と必ずしも同一ではありません。 ドキュメントの言語 ID を取得するには、次を使用します。

### <a name="method-isworkerthread"></a>メソッド isWorkerThread

セッションがワーカー スレッドかどうかを判定します。

    public boolean isWorkerThread()

#### <a name="return-value"></a>戻り値

セッションがワーカー スレッドである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

ワーカー スレッドは、Thread クラスのインスタンスで、UI がない Finance and Operations の新しいインスタンスを作成します。 このメソッドがこのようなセッション内で呼び出される場合は true が返されます。

### <a name="method-logindate"></a>メソッド loginDate

セッションのユーザーがログオンした日付を取得します。

    public Date loginDate()

#### <a name="return-value"></a>戻り値

セッションのユーザーがログオンした日付。

### <a name="method-logindatetime"></a>メソッド loginDateTime

    public DateTime loginDateTime()

#### <a name="return-value"></a>戻り値

### <a name="method-logintime"></a>メソッド loginTime

セッションのユーザーがログオンした時刻を取得します。

    public TimeOfDay loginTime()

#### <a name="return-value"></a>戻り値

セッションのユーザーがログオンした時間。

### <a name="method-mastersessionid"></a>メソッド masterSessionId

xSession オブジェクトの対象となるセッションのマスター セッション ID を取得します。

    public int masterSessionId()

#### <a name="return-value"></a>戻り値

セッション ID を表す整数。

#### <a name="remarks"></a>備考

一部のセッションには、COM セッションまたはワーカー スレッド セッションなどのマスター セッション ID があります。

#### <a name="examples"></a>例

次の例では、通常のセッション ID (または存在する場合は､マスター セッション ID) を使用して xSession オブジェクトを作成します。

    static xSession getThisSession() 
    { 
        xSession xSession = new xSession(sessionid()); 
        if (xSession.masterSessionId()) 
        { 
            xSession = new xSession(xSession.masterSessionId()); 
        } 
        return xSession; 
    }

### <a name="method-serverid"></a>メソッド serverId

    public int serverId()

#### <a name="return-value"></a>戻り値

### <a name="method-sessionid"></a>メソッド sessionId

xSession オブジェクトの対象となるセッションのセッション ID を取得します。

    public int sessionId()

#### <a name="return-value"></a>戻り値

セッション ID を表す整数。

### <a name="method-terminate"></a>メソッド terminate

オブジェクトのインスタンス化に使用されたセッション ID を終了します。

    public boolean terminate([Date loginDate], [TimeOfDay loginTime])

#### <a name="parameters"></a>パラメーター

loginDate  
セッションのユーザーがログオンした時間 (オプション)。

<!-- -->

loginTime  
セッションのユーザーがログオンした時間 (オプション)。

#### <a name="return-value"></a>戻り値

ユーザーにこの関数を実行する権限がない場合は false; それ以外の場合は true。

#### <a name="remarks"></a>備考

この API には、実行時に呼び出される組み込み認証チェックがあります。 終了メソッドの呼び出しが開発セキュリティ キー (SysDevelopment) のアクセス権のないユーザーによって行われた場合はスローされます。 オプションのパラメーターを使用すると、セッションにタイムスタンプを設定して、終了する予定のセッションであることを確認できます。 同じセッション ID を 2 つの異なる時間に使用することができます。 terminate メソッドは、オンライン ユーザー フォームで管理者がセッションを終了できるようにするために使用されます。 管理者はセッションが応答を停止した場合や、多くのリソースを消費した場合、または別のユーザーのためにライセンスを解放する必要がある場合にセッションを終了させることがあります。

#### <a name="examples"></a>例

次の例では、ユーザーにセッションを終了する権限があるかどうかを確認します。 その場合は、セッションが終了します。

    server static public void Main(Args _args) 
    { 
        Session session; 
        session = new Session(); 
        if (session) 
        { 
            session.terminate(); 
        } 
    }

### <a name="method-userid"></a>メソッド userId

このセッションがログオンしているユーザー ID を取得します。

    public UserId userId()

#### <a name="return-value"></a>戻り値

セッションのユーザーの ID です。

#### <a name="examples"></a>例

次の例では、特定のユーザーがオンラインかどうかを判断します。

    server static boolean isUserOnline(userId userId) 
    { 
        xSession    session; 
        int counter; 
        int maxSessions = Info::licensedUsersTotal(); 
        if (!userId) 
        { 
            return false; 
        } 
        for(counter = 1; counter < maxSessions;counter++) 
        { 
            session = new xSession(counter, true); 
            if(session && session.userId() == userId) 
            { 
                return true; 
            } 
        } 
        return false; 
    }

### <a name="method-currentretrycount"></a>メソッド currentRetryCount

デッドロック、更新の競合、または別の例外の後に try ブロックが再試行された回数をカウントします。

    public static int currentRetryCount()

#### <a name="return-value"></a>戻り値

try ブロックが再試行された回数。

#### <a name="examples"></a>例

次の例では、currentRetryCount メソッドを使用して、トランザクションが CUD トランザクションの例外処理を判断するために再試行された回数をテストします。

    catch (Exception::UpdateConflict) 
        { 
            if (appl.ttsLevel() == 0) 
            { 
                if (xSession::currentRetryCount() >= #RetryNum) 
                { 
                    throw Exception::UpdateConflictNotRecovered; 
                } 
                else 
                { 
                    retry; 
                } 
            } 
            else 
            { 
                throw Exception::UpdateConflict; 
            } 
        }

### <a name="method-currentuncheck"></a>メソッド currentUnCheck

    public static Uncheck currentUnCheck()

#### <a name="return-value"></a>戻り値

### <a name="method-getdbschema"></a>メソッド getDbSchema

セッションのデータベース オブジェクト名のスキーマ部分を取得します。

    public static str getDbSchema()

#### <a name="return-value"></a>戻り値

データベース オブジェクト名のスキーマ部分を返します。

### <a name="method-getiisobject"></a>メソッド getIISObject

IIS オブジェクトの COM オブジェクトのインスタンスを作成して返します。

    public static COM getIISObject(IISObject object)

#### <a name="parameters"></a>パラメーター

オブジェクト  
COM オブジェクトを作成する IIS オブジェクト。

#### <a name="return-value"></a>戻り値

COM オブジェクト。

#### <a name="remarks"></a>備考

IIS オブジェクトは、IISObject システム列挙によって提供される使用可能な値のいずれかにすることができます。

-   ApplicationObject
-   要求
-   応答
-   サーバー
-   SessionObject

### <a name="method-getsystraceactive"></a>メソッド getSysTraceActive

セッションでシステム トレースを有効にするかどうかを決定できます。

    public static boolean getSysTraceActive()

#### <a name="return-value"></a>戻り値

システム トレースが有効な場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

システム トレースを有効にするには、xSession::setSysTraceActive を使用します。

#### <a name="examples"></a>例

次の例では、getSysTraceActive メソッドを使用してシステム トレースの元の設定を判断し、トレースを一時的に false に設定した後に設定をリセットします。

    server static void main(Args a) 
    { 
        SysDataImport sysDataImport; 
        boolean       sysTraceActive = xSession::getSysTraceActive(); 
        sysDataImport = SysDataImport::newTmpFilename(''); 
        sysDataImport.addTmpExpImpTable( 
            tablenum(SysTraceTableSQL), 
            false); 
        sysDataImport.addTmpExpImpTable( 
            tablenum(SysTraceTableSQLExecPlan), 
            false); 
        sysDataImport.addTmpExpImpTable( 
            tablenum(SysTraceTableSQLTabRef), 
            false); 
        xSession::setSysTraceActive(FALSE); 
        if (sysDataImport.prompt()) 
            sysDataImport.run(); 
        xSession::setSysTraceActive(sysTraceActive); 
    }

### <a name="method-getxrefassembytempfolder"></a>メソッド getXRefAssembyTempFolder

    public static str getXRefAssembyTempFolder()

#### <a name="return-value"></a>戻り値

### <a name="method-isclrsession"></a>メソッド isCLRSession

    public static boolean isCLRSession()

#### <a name="return-value"></a>戻り値

### <a name="method-isuserpreferredtzsameaslocalmachine"></a>メソッド isUserPreferredTzSameAsLocalMachine

    public static boolean isUserPreferredTzSameAsLocalMachine()

#### <a name="return-value"></a>戻り値

### <a name="method-lastduplicatekeyviolatingtable"></a>メソッド lastDuplicateKeyViolatingTable

    public static int lastDuplicateKeyViolatingTable()

#### <a name="return-value"></a>戻り値

### <a name="method-lastupdateconflictingtable"></a>メソッド lastUpdateConflictingTable

最後に更新の競合をしたテーブルのインスタンスを取得します。

    public static int lastUpdateConflictingTable()

#### <a name="return-value"></a>戻り値

最後に、更新の競合をしたテーブルのインスタンス。

#### <a name="examples"></a>例

次の例では、lastUpdateConflictingTable メソッドの一般的な使用方法を示しています。これにより、更新の競合が発生しているテーブルに従ってトランザクションを中断または再試行できます。

    try 
    { 
        // ... 
        table1.update(); 
        // ... 
        table2.update(); 
    } 
    catch(Exception::UpdateConflict) 
    { 
        if(xSession::lastUpdateConflictingTable() == table1) 
        { 
            ttsabort; 
        } 
        else if(xSession::lastUpdateConflictingTable() == table2) 
        { 
            // Compensate here. 
            // ... 
            retry; 
        } 
    }

### <a name="method-maxsessionid"></a>メソッド maxSessionId

現在のライセンス コードで許可されているセッションの最大数を取得します。

    public static int maxSessionId()

#### <a name="return-value"></a>戻り値

現在のライセンス コードで許可されているセッションの最大数を示す整数。

### <a name="method-numsession"></a>メソッド numSession

登録されているセッションの現在の番号を取得します。

    public static int numSession()

#### <a name="return-value"></a>戻り値

現在登録されているセッションの数を示す整数。

### <a name="method-preferredlocale"></a>メソッド preferredLocale

    public PreferredLocale preferredLocale()

#### <a name="return-value"></a>戻り値

### <a name="method-pseudobandwidth"></a>メソッド pseudoBandwidth

セッションの帯域幅シミュレーションをオンにするかどうかを決定し、帯域幅シミュレーションをオンまたはオフにします。

    public static int pseudoBandwidth([int bandwidth])

#### <a name="parameters"></a>パラメーター

bandwidth  
帯域幅のシミュレーションのオン/オフを切り替えます。 シミュレーションをオフにするには 0 に設定されます。 その他の値は、シミュレーションをオンにします。

#### <a name="return-value"></a>戻り値

帯域幅のシミュレーションを有効にするかどうかを示す整数。 戻り値が 0 の場合、帯域幅シミュレーションはありません。

#### <a name="remarks"></a>備考

システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。

-   ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。

### <a name="method-pseudolatency"></a>メソッド pseudoLatency

セッションの待機シミュレーションをオンにするかどうかを決定し、待機シミュレーションをオンまたはオフにします。

    public static int pseudoLatency([int latency])

#### <a name="parameters"></a>パラメーター

latency  
待機シミュレーションのオン/オフを切り替えます。 シミュレーションをオフにするには 0 に設定されます。 その他の値は、シミュレーションをオンにします。

#### <a name="return-value"></a>戻り値

待機シミュレーションを有効にするかどうかを示す整数。 戻り値が 0 の場合、遅延シミュレーションはありません。

#### <a name="remarks"></a>備考

システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。

-   ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。

### <a name="method-pseudosimmode"></a>メソッド pseudoSimMode

セッションの遅延シミュレーションをオンにするかどうかを決定し、遅延シミュレーションをオンまたはオフにします。

    public static int pseudoSimMode([int simMode])

#### <a name="parameters"></a>パラメーター

simMode  
遅延シミュレーションのオン/オフを切り替えます。 シミュレーションをオフにするには 0 に設定されます。 アプリケーションの呼び出しで遅延をシミュレートするには 1 に設定します。 すべての呼び出しで遅延をシミュレートするには 2 に設定します。

#### <a name="return-value"></a>戻り値

遅延シミュレーションを有効にするかどうかを示す整数。 戻り値が 0 の場合、遅延シミュレーションはありません。 戻り値が 1 の場合は、遅延はアプリケーション制御の呼び出しに対してのみシミュレートされます。 戻り値が 2 の場合は、遅延はすべての呼び出しに対してシミュレートされます。

#### <a name="remarks"></a>備考

システム監視ツールからリモート接続の疑似シミュレーションを実行することができます。

-   ツール バーで、ツールを選択し、開発ツールをポイントし、システム監視をポイントして、リモート接続タブをクリックします。

### <a name="method-systemsessionid"></a>メソッド systemSessionId

xSession オブジェクトの対象となるセッションのシステム セッション ID を取得します。

    public static int systemSessionId()

#### <a name="return-value"></a>戻り値

セッション ID を表す整数。

#### <a name="remarks"></a>備考

COM セッションまたはワーカー スレッド セッションなどの一部のセッションには、親システム セッションがあります。

### <a name="method-xppcallstack"></a>メソッド xppCallStack

現在の呼び出し履歴を取得します。

    public static container xppCallStack()

#### <a name="return-value"></a>戻り値

現在のコール スタックの内容を保持するコンテナーです。

### <a name="method-removeaoc"></a>メソッド removeAOC

現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を削除します。

    public static void removeAOC()

### <a name="method-updateaoc"></a>メソッド updateAOC

現在のセッションの Application Object Server のクライアント側キャッシュ (AOC) を更新します。

    public static void updateAOC()

#### <a name="remarks"></a>備考

AOC は、クライアントによってロードされるメタデータで構成されるクライアント側のキャッシュであり、クライアントを閉じると、ディスクに保存されます。 これはユーザーのローカル設定フォルダーで保存されます。 このファイルの拡張子は .auc で、ユーザーのローカル設定フォルダーに保存されます。 クライアントは、起動されると、キャッシュからの読み取りの後、ディスクからそのキャッシュを削除します。

### <a name="method-setautoupdaterecversion"></a>メソッド setAutoUpdateRecVersion

    public static void setAutoUpdateRecVersion(boolean autoUpdateRecVersion)

#### <a name="parameters"></a>パラメーター

autoUpdateRecVersion  

### <a name="method-setsystraceactive"></a>メソッド setSysTraceActive

システム追跡のオンまたはオフを切り替えます。

    public static void setSysTraceActive(boolean nValue)

#### <a name="parameters"></a>パラメーター

nValue  
追跡をオンまたはオフに切り替える必要があるかどうかを指定するブール値。 追跡をオンにするには、true に設定します。

#### <a name="examples"></a>例

次の例では、データのインポート時に setSysTraceActive メソッドを使用してシステム トレースをオフにします。

    server static void main(Args a) 
    { 
        SysDataImport sysDataImport; 
        boolean       sysTraceActive = xSession::getSysTraceActive(); 
        sysDataImport = SysDataImport::newTmpFilename(''); 
        sysDataImport.addTmpExpImpTable( 
            tablenum(SysTraceTableSQL), 
            false); 
        sysDataImport.addTmpExpImpTable( 
            tablenum(SysTraceTableSQLExecPlan), 
            false); 
        sysDataImport.addTmpExpImpTable( 
            tablenum(SysTraceTableSQLTabRef), 
            false); 
        xSession::setSysTraceActive(FALSE); 
        if (sysDataImport.prompt()) 
            sysDataImport.run(); 
        xSession::setSysTraceActive(sysTraceActive); 
    }

### <a name="method-clientsetautoupdaterecversion"></a>メソッド clientSetAutoUpdateRecVersion

    private static void clientSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)

#### <a name="parameters"></a>パラメーター

autoUpdateRecVersion  

### <a name="method-serversetautoupdaterecversion"></a>メソッド serverSetAutoUpdateRecVersion

    private static void serverSetAutoUpdateRecVersion(boolean autoUpdateRecVersion)

#### <a name="parameters"></a>パラメーター

autoUpdateRecVersion  

### <a name="method-new"></a>メソッド new

現在のセッションまたはパラメーターとして渡されたセッション ID のいずれかに対して xSession オブジェクトのインスタンスを作成します。

    public void new([int sessionId], [boolean checkSession])

#### <a name="parameters"></a>パラメーター

sessionId  
true に設定すると\_SessionId パラメーターで指定されたセッションが存在するかどうかを確認するブール フラグ。 セッションが存在するかどうかを確認する操作は、多くのシステムリソースを使用する可能性があります。 したがって、このパラメーターは既定で false に設定されています。

<!-- -->

checkSession  
true に設定すると\_SessionId パラメーターで指定されたセッションが存在するかどうかを確認するブール フラグ。 セッションが存在するかどうかを確認する操作は、多くのシステムリソースを使用する可能性があります。 したがって、このパラメーターは既定で false に設定されています。

#### <a name="examples"></a>例

次の例は、すべての有効なセッションの数を返します。

    server static Integer getAllOnlineUserCount() 
    { 
        int      counter; 
        int      num = 0; 
        int      maxSessions = Info::licensedUsersTotal(); 
        xSession session; 
        UserInfo userInfo; 
        for(counter = 1; counter < maxSessions;counter++) 
        { 
            session = new xSession(counter, true); 
            if(session && session.userId()) 
            { 
                select firstonly userInfo 
                    where userInfo.Id == session.userId(); 
                if (userInfo) 
                    num++; 
            } 
        } 
        return num; 
    }

### <a name="method-reloadtablecollectiononclient"></a>メソッド reloadTableCollectionOnClient

    public static void reloadTableCollectionOnClient()

## <a name="class-xsqlenumerator"></a>クラス xSqlEnumerator
    class xSqlEnumerator extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                               | 説明                                             |
|------------------------------------------------------|---------------------------------------------------------|
| public str getConnStr(str database)                  |                                                         |
| public List getDatabases(str server, \[str driver\]) |                                                         |
| public List getServers(str driver)                   |                                                         |
| public void new()                                    | xSqlEnumerator クラスの新しいインスタンスを初期化します。 |

### <a name="method-getconnstr"></a>メソッド getConnStr

    public str getConnStr(str database)

#### <a name="parameters"></a>パラメーター

データベース  

#### <a name="return-value"></a>戻り値

### <a name="method-getdatabases"></a>メソッド getDatabases

    public List getDatabases(str server, [str driver])

#### <a name="parameters"></a>パラメーター

server  

<!-- -->

driver  

#### <a name="return-value"></a>戻り値

### <a name="method-getservers"></a>メソッド getServers

    public List getServers(str driver)

#### <a name="parameters"></a>パラメーター

driver  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

xSqlEnumerator クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-xtoastnotification"></a>クラス xToastNotification
    class xToastNotification extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                      | 説明                                                 |
|---------------------------------------------|-------------------------------------------------------------|
| public int duration(\[int duration\])       |                                                             |
| public int imageResId(\[int imageResId\])   |                                                             |
| public str messageText(\[str messageText\]) |                                                             |
| public str subject(\[str subject\])         |                                                             |
| public void new()                           | xToastNotification クラスの新しいインスタンスを初期化します。 |
| public void onClosed()                      |                                                             |
| public void show()                          |                                                             |
| public void finalize()                      |                                                             |
| public void onClicked()                     |                                                             |

### <a name="method-duration"></a>メソッド duration

    public int duration([int duration])

#### <a name="parameters"></a>パラメーター

duration  

#### <a name="return-value"></a>戻り値

### <a name="method-imageresid"></a>メソッド imageResId

    public int imageResId([int imageResId])

#### <a name="parameters"></a>パラメーター

imageResId  

#### <a name="return-value"></a>戻り値

### <a name="method-messagetext"></a>メソッド messageText

    public str messageText([str messageText])

#### <a name="parameters"></a>パラメーター

messageText  

#### <a name="return-value"></a>戻り値

### <a name="method-subject"></a>メソッド subject

    public str subject([str subject])

#### <a name="parameters"></a>パラメーター

subject  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

xToastNotification クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-onclosed"></a>メソッド onClosed

    public void onClosed()

### <a name="method-show"></a>メソッド show

    public void show()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-onclicked"></a>メソッド onClicked

    public void onClicked()

## <a name="class-xversioncontrol"></a>クラス xVersionControl
    class xVersionControl extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                            | 説明                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| public boolean allowCreate(TreeNode node)                                                                                                                         |                                                          |
| public boolean allowDelete(TreeNode node)                                                                                                                         |                                                          |
| public boolean allowEdit(TreeNode node)                                                                                                                           |                                                          |
| public boolean allowRename(TreeNode node)                                                                                                                         |                                                          |
| public boolean checkOut(TreeNode node)                                                                                                                            |                                                          |
| public boolean create(TreeNode node)                                                                                                                              |                                                          |
| public boolean delete(TreeNode node)                                                                                                                              |                                                          |
| public int getAvailableId(UtilElementType objectType, UtilEntryLevel layer, \[int parentId\], \[IdAllocationSchema idAllocationSchema\], \[boolean inheritance\]) |                                                          |
| public int getAvailableLabelId(str labelFile, str language, \[IdAllocationSchema idAllocationSchema\])                                                            |                                                          |
| public boolean ideIntegration()                                                                                                                                   |                                                          |
| public boolean moveToModel(TreeNode node, int modelId)                                                                                                            |                                                          |
| public boolean rename(TreeNode node, str newname)                                                                                                                 |                                                          |
| public boolean undoCheckOut(TreeNode node, \[boolean showDialog\])                                                                                                |                                                          |
| public Set unwantedObjectTypes()                                                                                                                                  |                                                          |
| public void colorAOT()                                                                                                                                            |                                                          |
| public void save(TreeNode node)                                                                                                                                   |                                                          |
| public void showHistory(TreeNode node)                                                                                                                            |                                                          |
| public void updateCheckedOutList(Set checkedOutObjects)                                                                                                           |                                                          |
| public void getLatestVersion(\[TreeNode node\], \[boolean delLocalFiles\])                                                                                        |                                                          |
| public void checkIn(TreeNode node)                                                                                                                                |                                                          |
| public void new()                                                                                                                                                 | xVersionControl クラスの新しいインスタンスを初期化します。 |
| public void reload()                                                                                                                                              |                                                          |
| public void getLabelVersion(\[TreeNode node\], \[str label\])                                                                                                     |                                                          |

### <a name="method-allowcreate"></a>メソッド allowCreate

    public boolean allowCreate(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-allowdelete"></a>メソッド allowDelete

    public boolean allowDelete(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

    public boolean allowEdit(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-allowrename"></a>メソッド allowRename

    public boolean allowRename(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-checkout"></a>メソッド checkOut

    public boolean checkOut(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-create"></a>メソッド create

    public boolean create(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-delete"></a>メソッド delete

    public boolean delete(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-getavailableid"></a>メソッド getAvailableId

    public int getAvailableId(UtilElementType objectType, UtilEntryLevel layer, [int parentId], [IdAllocationSchema idAllocationSchema], [boolean inheritance])

#### <a name="parameters"></a>パラメーター

objectType  

<!-- -->

 レイヤー  

<!-- -->

parentId  

<!-- -->

idAllocationSchema  

<!-- -->

inheritance  

#### <a name="return-value"></a>戻り値

### <a name="method-getavailablelabelid"></a>メソッド getAvailableLabelId

    public int getAvailableLabelId(str labelFile, str language, [IdAllocationSchema idAllocationSchema])

#### <a name="parameters"></a>パラメーター

labelFile  

<!-- -->

言語  

<!-- -->

idAllocationSchema  

#### <a name="return-value"></a>戻り値

### <a name="method-ideintegration"></a>メソッド ideIntegration

    public boolean ideIntegration()

#### <a name="return-value"></a>戻り値

### <a name="method-movetomodel"></a>メソッド moveToModel

    public boolean moveToModel(TreeNode node, int modelId)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

modelId  

#### <a name="return-value"></a>戻り値

### <a name="method-rename"></a>メソッド rename

    public boolean rename(TreeNode node, str newname)

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

newname  

#### <a name="return-value"></a>戻り値

### <a name="method-undocheckout"></a>メソッド undoCheckOut

    public boolean undoCheckOut(TreeNode node, [boolean showDialog])

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

showDialog  

#### <a name="return-value"></a>戻り値

### <a name="method-unwantedobjecttypes"></a>メソッド unwantedObjectTypes

    public Set unwantedObjectTypes()

#### <a name="return-value"></a>戻り値

### <a name="method-coloraot"></a>メソッド colorAOT

    public void colorAOT()

### <a name="method-save"></a>メソッド save

    public void save(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-showhistory"></a>メソッド showHistory

    public void showHistory(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-updatecheckedoutlist"></a>メソッド updateCheckedOutList

    public void updateCheckedOutList(Set checkedOutObjects)

#### <a name="parameters"></a>パラメーター

checkedOutObjects  

### <a name="method-getlatestversion"></a>メソッド getLatestVersion

    public void getLatestVersion([TreeNode node], [boolean delLocalFiles])

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

delLocalFiles  

### <a name="method-checkin"></a>メソッド checkIn

    public void checkIn(TreeNode node)

#### <a name="parameters"></a>パラメーター

node  

### <a name="method-new"></a>メソッド new

xVersionControl クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-reload"></a>メソッド reload

    public void reload()

### <a name="method-getlabelversion"></a>メソッド getLabelVersion

    public void getLabelVersion([TreeNode node], [str label])

#### <a name="parameters"></a>パラメーター

node  

<!-- -->

ラベル  





