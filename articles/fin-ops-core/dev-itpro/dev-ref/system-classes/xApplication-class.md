---
title: xApplication クラス
description: このトピックでは、xApplication クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cea63cb01203d41a385d241633aa53a1a96d5779
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502682"
---
# <a name="class-xapplication"></a>クラス xApplication

[!include [banner](../../includes/banner.md)]


```xpp
class xApplication extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-istableperhierarchymode"></a>メソッド IsTablePerHierarchyMode

すべてのテーブルの継承階層をフラットにしてシステムを実行するかどうかを決定します (階層ごとの表モード)。

```xpp
public boolean IsTablePerHierarchyMode()
```

### <a name="return-value---istableperhierarchymode"></a>戻り値 - IsTablePerHierarchyMode

システムが階層別テーブル モードで実行されている場合は true。それ以外の場合は、false。

## <a name="method-buildno"></a>メソッド buildNo

```xpp
public str buildNo()
```

### <a name="return-value---buildno"></a>戻り値 - buildNo

## <a name="method-candeletecompany"></a>メソッド canDeleteCompany

```xpp
public boolean canDeleteCompany(SelectableDataArea company)
```

### <a name="parameters---candeletecompany"></a>パラメーター - canDeleteCompany

会社  

### <a name="return-value---candeletecompany"></a>戻り値 - canDeleteCompany

## <a name="method-countoftoplevelformsopened"></a>メソッド countOfTopLevelFormsOpened

```xpp
public int countOfTopLevelFormsOpened()
```

### <a name="return-value---countoftoplevelformsopened"></a>戻り値 - countOfTopLevelFormsOpened

## <a name="method-company"></a>メソッド company

```xpp
public Company company([SelectableDataArea company])
```

### <a name="parameters---company"></a>パラメーター - company

会社  

### <a name="return-value---company"></a>戻り値 - company

## <a name="method-curtransactionid"></a>メソッド curTransactionId

```xpp
public Int64 curTransactionId([boolean ForceTakeNumber])
```

### <a name="parameters---curtransactionid"></a>パラメーター - curTransactionId

ForceTakeNumber  

### <a name="return-value---curtransactionid"></a>戻り値 - curTransactionId

## <a name="method-dbsynchronize"></a>メソッド dbSynchronize

```xpp
public boolean dbSynchronize([TableId tableId], [boolean checkAsNeeded], [boolean continueOnError], [boolean showProgress], [container checkSyncTables], [boolean createAllIndexes], [boolean useLockForSingleTable])
```

### <a name="parameters---dbsynchronize"></a>パラメーター - dbSynchronize

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

### <a name="return-value---dbsynchronize"></a>戻り値 - dbSynchronize

## <a name="method-getsamenamedifferentidfields"></a>メソッド getSameNameDifferentIdFields

```xpp
public str getSameNameDifferentIdFields()
```

### <a name="return-value---getsamenamedifferentidfields"></a>戻り値 - getSameNameDifferentIdFields

## <a name="method-getservicehoststatus"></a>メソッド getServiceHostStatus

```xpp
public Map getServiceHostStatus()
```

### <a name="return-value---getservicehoststatus"></a>戻り値 - getServiceHostStatus

## <a name="method-ischeckedmode"></a>メソッド isCheckedMode

```xpp
public boolean isCheckedMode()
```

### <a name="return-value---ischeckedmode"></a>戻り値 - isCheckedMode

## <a name="method-isconfigmode"></a>メソッド isConfigMode

```xpp
public boolean isConfigMode()
```

### <a name="return-value---isconfigmode"></a>戻り値 - isConfigMode

## <a name="method-isdemomode"></a>メソッド isDemoMode

```xpp
public boolean isDemoMode()
```

### <a name="return-value---isdemomode"></a>戻り値 - isDemoMode

## <a name="method-issqlconnected"></a>メソッド isSqlConnected

```xpp
public boolean isSqlConnected()
```

### <a name="return-value---issqlconnected"></a>戻り値 - isSqlConnected

## <a name="method-numberoftreenodesloaded"></a>メソッド numberOfTreeNodesLoaded

```xpp
public int numberOfTreeNodesLoaded()
```

### <a name="return-value---numberoftreenodesloaded"></a>戻り値 - numberOfTreeNodesLoaded

## <a name="method-releaseversion"></a>メソッド releaseVersion

```xpp
public str releaseVersion()
```

### <a name="return-value---releaseversion"></a>戻り値 - releaseVersion

## <a name="method-setdefaultcompany"></a>メソッド setDefaultCompany

```xpp
public boolean setDefaultCompany(SelectableDataArea company)
```

### <a name="parameters---setdefaultcompany"></a>パラメーター - setDefaultCompany

会社  

### <a name="return-value---setdefaultcompany"></a>戻り値 - setDefaultCompany

## <a name="method-ttslevel"></a>メソッド ttsLevel

```xpp
public int ttsLevel()
```

### <a name="return-value---ttslevel"></a>戻り値 - ttsLevel

## <a name="method-ttsversion"></a>メソッド ttsVersion

```xpp
public int ttsVersion()
```

### <a name="return-value---ttsversion"></a>戻り値 - ttsVersion

## <a name="method-checkuserexistsinanypartition"></a>メソッド CheckUserExistsInAnyPartition

指定されたユーザーがどのパーティションにも存在するかどうかをチェックします。

```xpp
public static boolean CheckUserExistsInAnyPartition(str userId)
```

### <a name="parameters---checkuserexistsinanypartition"></a>パラメーター - CheckUserExistsInAnyPartition

userId  

### <a name="return-value---checkuserexistsinanypartition"></a>戻り値 - CheckUserExistsInAnyPartition

ユーザーがいずれかのパーティションに存在する場合は true。それ以外の場合は、false。

## <a name="method-getfolderpath"></a>メソッド getFolderPath

```xpp
public static str getFolderPath(int folder)
```

### <a name="parameters---getfolderpath"></a>パラメーター - getFolderPath

folder  

### <a name="return-value---getfolderpath"></a>戻り値 - getFolderPath

## <a name="method-getvsassembliespath"></a>メソッド getVSAssembliesPath

```xpp
public static str getVSAssembliesPath()
```

### <a name="return-value---getvsassembliespath"></a>戻り値 - getVSAssembliesPath

## <a name="method-ilcachecontains"></a>メソッド ilCacheContains

```xpp
public static boolean ilCacheContains(str owner, str key)
```

### <a name="parameters---ilcachecontains"></a>パラメーター - ilCacheContains

所有者  

<!-- -->

キー  

### <a name="return-value---ilcachecontains"></a>戻り値 - ilCacheContains

## <a name="method-ilcachedelete"></a>メソッド ilCacheDelete

```xpp
public static str ilCacheDelete(str owner, str key)
```

### <a name="parameters---ilcachedelete"></a>パラメーター - ilCacheDelete

所有者  

<!-- -->

キー  

### <a name="return-value---ilcachedelete"></a>戻り値 - ilCacheDelete

## <a name="method-ilcachefind"></a>メソッド ilCacheFind

```xpp
public static str ilCacheFind(str owner, str key)
```

### <a name="parameters---ilcachefind"></a>パラメーター - ilCacheFind

所有者  

<!-- -->

キー  

### <a name="return-value---ilcachefind"></a>戻り値 - ilCacheFind

## <a name="method-initpartition"></a>メソッド initPartition

DAT 会社と管理者ユーザーを作成することで指定したパーティションを初期化します。

```xpp
public static boolean initPartition(Partition partition)
```

### <a name="parameters---initpartition"></a>パラメーター - initPartition

パーティション  
初期化するパーティションのレコード ID。

### <a name="return-value---initpartition"></a>戻り値 - initPartition

初期化が成功した場合は true。それ以外の場合は、false。

### <a name="remarks---initpartition"></a>備考 - initPartition

この API は、アップグレード フレームワークでのみ使用されます。 それを他のコンテキストで使用すると、データに回復不能な影響が発生することがあります。

## <a name="method-isserviceregisteredonclient"></a>メソッド isServiceRegisteredOnClient

```xpp
public static boolean isServiceRegisteredOnClient(ClassId classId)
```

### <a name="parameters---isserviceregisteredonclient"></a>パラメーター - isServiceRegisteredOnClient

classId  

### <a name="return-value---isserviceregisteredonclient"></a>戻り値 - isServiceRegisteredOnClient

## <a name="method-issinglepartitionsystem"></a>メソッド IsSinglePartitionSystem

配置が単一のパーティションか複数パーティションかを評価します。

```xpp
public static boolean IsSinglePartitionSystem()
```

### <a name="return-value---issinglepartitionsystem"></a>戻り値 - IsSinglePartitionSystem

展開にパーティションが 1 つのみある場合は true。展開に複数のパーティションがある場合は false。

## <a name="method-xppilappdomain"></a>メソッド XppILAppDomain

```xpp
public static CLRObject XppILAppDomain()
```

### <a name="return-value---xppilappdomain"></a>戻り値 - XppILAppDomain

## <a name="method-isintransactionscope"></a>メソッド isInTransactionScope

```xpp
public boolean isInTransactionScope()
```

### <a name="return-value---isintransactionscope"></a>戻り値 - isInTransactionScope

## <a name="method-transactionscopecommitlevel"></a>メソッド transactionScopeCommitLevel

```xpp
public Int64 transactionScopeCommitLevel()
```

### <a name="return-value---transactionscopecommitlevel"></a>戻り値 - transactionScopeCommitLevel

## <a name="method-encrypt"></a>メソッド Encrypt

```xpp
public container Encrypt(str input)
```

### <a name="parameters---encrypt"></a>パラメーター - Encrypt

入力  

### <a name="return-value---encrypt"></a>戻り値 - Encrypt

## <a name="method-decrypt"></a>メソッド Decrypt

```xpp
public str Decrypt(container cipher)
```

### <a name="parameters---decrypt"></a>パラメーター - Decrypt

cipher  

### <a name="return-value---decrypt"></a>戻り値 - Decrypt

## <a name="method-decrypttosecurestring"></a>メソッド decryptToSecureString

```xpp
public System.Security.SecureString decryptToSecureString(container cipher)
```

### <a name="parameters---decrypttosecurestring"></a>パラメーター - decryptToSecureString

cipher  

### <a name="return-value---decrypttosecurestring"></a>戻り値 - decryptToSecureString

## <a name="method-encryptfromsecurestring"></a>メソッド encryptFromSecureString

```xpp
public container encryptFromSecureString(System.Security.SecureString input)
```

### <a name="parameters---encryptfromsecurestring"></a>パラメーター - encryptFromSecureString

入力  

### <a name="return-value---encryptfromsecurestring"></a>戻り値 - encryptFromSecureString

## <a name="method-encryptforpurpose"></a>メソッド EncryptForPurpose

```xpp
public container EncryptForPurpose(str input, str purpose)
```

### <a name="parameters---encryptforpurpose"></a>パラメーター - EncryptForPurpose

入力  

<!-- -->

purpose  

### <a name="return-value---encryptforpurpose"></a>戻り値 - EncryptForPurpose

## <a name="method-decryptforpurpose"></a>メソッド DecryptForPurpose

```xpp
public str DecryptForPurpose(container cipher, str purpose)
```

### <a name="parameters---decryptforpurpose"></a>パラメーター - DecryptForPurpose

cipher  

<!-- -->

purpose  

### <a name="return-value---decryptforpurpose"></a>戻り値 - DecryptForPurpose

## <a name="method-decrypttosecurestringforpurpose"></a>メソッド decryptToSecureStringForPurpose

```xpp
public System.Security.SecureString decryptToSecureStringForPurpose(container cipher, str purpose)
```

### <a name="parameters---decrypttosecurestringforpurpose"></a>パラメーター - decryptToSecureStringForPurpose

cipher  

<!-- -->

purpose  

### <a name="return-value---decrypttosecurestringforpurpose"></a>戻り値 - decryptToSecureStringForPurpose

## <a name="method-encryptfromsecurestringforpurpose"></a>メソッド encryptFromSecureStringForPurpose

```xpp
public container encryptFromSecureStringForPurpose(System.Security.SecureString input, str purpose)
```

### <a name="parameters---encryptfromsecurestringforpurpose"></a>パラメーター - encryptFromSecureStringForPurpose

入力  

<!-- -->

purpose  

### <a name="return-value---encryptfromsecurestringforpurpose"></a>戻り値 - encryptFromSecureStringForPurpose

## <a name="method-converttounsecurestring"></a>メソッド convertToUnsecureString

```xpp
public str convertToUnsecureString(System.Security.SecureString secureString)
```

### <a name="parameters---converttounsecurestring"></a>パラメーター - convertToUnsecureString

secureString  

### <a name="return-value---converttounsecurestring"></a>戻り値 - convertToUnsecureString

## <a name="method-converttosecurestring"></a>メソッド convertToSecureString

```xpp
public System.Security.SecureString convertToSecureString(str unsecureString)
```

### <a name="parameters---converttosecurestring"></a>パラメーター - convertToSecureString

unsecureString  

### <a name="return-value---converttosecurestring"></a>戻り値 - convertToSecureString

## <a name="method-startbatch"></a>メソッド startBatch

```xpp
public static void startBatch()
```

## <a name="method-deletecompany"></a>メソッド deleteCompany

```xpp
public void deleteCompany(SelectableDataArea company)
```

### <a name="parameters---deletecompany"></a>パラメーター - deleteCompany

会社  

## <a name="method-ttsabort"></a>メソッド ttsabort

```xpp
public void ttsabort()
```

## <a name="method-transactionscopecommit"></a>メソッド transactionScopeCommit

```xpp
public void transactionScopeCommit()
```

## <a name="method-new"></a>メソッド new

xApplication クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-stopbatch"></a>メソッド stopBatch

```xpp
public static void stopBatch()
```

## <a name="method-logrenamekey"></a>メソッド logRenameKey

```xpp
public void logRenameKey(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---logrenamekey"></a>パラメーター - logRenameKey

recordOrig  

<!-- -->

recordUpdated  

<!-- -->

changedFields  

## <a name="method-startup"></a>メソッド startup

```xpp
public void startup(str startupCmd, str buildNumber)
```

### <a name="parameters---startup"></a>パラメーター - startup

startupCmd  

<!-- -->

buildNumber  

## <a name="method-redirecttodashboard"></a>メソッド RedirectToDashboard

```xpp
public void RedirectToDashboard()
```

## <a name="method-insertxreferences"></a>メソッド insertXReferences

相互参照情報をデータベースに挿入する必要があるときに、フレームワークによって呼び出されます。

```xpp
public void insertXReferences()
```

### <a name="remarks---insertxreferences"></a>備考 - insertXReferences

Application クラスは、過負荷機能を提供します。

## <a name="method-logupdate"></a>メソッド logUpdate

```xpp
public void logUpdate(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---logupdate"></a>パラメーター - logUpdate

recordOrig  

<!-- -->

recordUpdated  

<!-- -->

changedFields  

## <a name="method-setstartpage"></a>メソッド setStartPage

```xpp
public void setStartPage([SysUserInfoStartPage startpage])
```

### <a name="parameters---setstartpage"></a>パラメーター - setStartPage

startpage  

## <a name="method-ilcacheinsert"></a>メソッド ilCacheInsert

```xpp
public static void ilCacheInsert(str owner, str key, str value)
```

### <a name="parameters---ilcacheinsert"></a>パラメーター - ilCacheInsert

所有者  

<!-- -->

キー  

<!-- -->

値  

## <a name="method-clearmanagedcaches"></a>メソッド clearManagedCaches

```xpp
public void clearManagedCaches()
```

## <a name="method-eventdelete"></a>メソッド eventDelete

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが削除されたときにカーネルにより呼び出されるコールバックとして機能します。

```xpp
public void eventDelete(Common recordDeleted)
```

### <a name="parameters---eventdelete"></a>パラメーター - eventDelete

recordDeleted  
削除したレコード。

### <a name="remarks---eventdelete"></a>備考 - eventDelete

開発者は、特定のテーブルの削除時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実現できます。これには、logType フィールドを EventDelete に設定することが含まれます。 これは、logDelete メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、レコードが削除されたトランザクション内にあります。

## <a name="method-enablecountrycontextfilter"></a>メソッド enableCountryContextFilter

現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を有効にします。

```xpp
public void enableCountryContextFilter()
```

## <a name="method-settheme"></a>メソッド setTheme

```xpp
public void setTheme([SysUserInfoTheme theme])
```

### <a name="parameters---settheme"></a>パラメーター - setTheme

theme  

## <a name="method-systrace"></a>メソッド sysTrace

```xpp
public void sysTrace(SysTraceType traceType, container traceInfo)
```

### <a name="parameters---systrace"></a>パラメーター - sysTrace

traceType  

<!-- -->

traceInfo  

## <a name="method-initglobal"></a>メソッド initGlobal

```xpp
public void initGlobal(Info infoObject, VersionControl versionControlObject)
```

### <a name="parameters---initglobal"></a>パラメーター - initGlobal

infoObject  

<!-- -->

versionControlObject  

## <a name="method-transactionscoperollback"></a>メソッド transactionScopeRollback

```xpp
public void transactionScopeRollback(Int64 commitLevel)
```

### <a name="parameters---transactionscoperollback"></a>パラメーター - transactionScopeRollback

commitLevel  

## <a name="method-ttsbegin"></a>メソッド ttsbegin

```xpp
public void ttsbegin()
```

## <a name="method-flushcompanycache"></a>メソッド flushcompanycache

```xpp
public void flushcompanycache(SelectableDataArea company)
```

### <a name="parameters---flushcompanycache"></a>パラメーター - flushcompanycache

会社  

## <a name="method-logdelete"></a>メソッド logDelete

```xpp
public void logDelete(Common recordDeleted)
```

### <a name="parameters---logdelete"></a>パラメーター - logDelete

recordDeleted  

## <a name="method-registerserviceonclient"></a>メソッド registerServiceOnClient

```xpp
public static void registerServiceOnClient(ClassId classId, str externalName)
```

### <a name="parameters---registerserviceonclient"></a>パラメーター - registerServiceOnClient

classId  

<!-- -->

externalName  

## <a name="method-eventupdate"></a>メソッド eventUpdate

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが更新されたときにカーネルにより呼び出されるコールバックとして機能します。

```xpp
public void eventUpdate(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---eventupdate"></a>パラメーター - eventUpdate

recordOrig  
すべての変更されたフィールドのコンテナーです。

<!-- -->

recordUpdated  
すべての変更されたフィールドのコンテナーです。

<!-- -->

changedFields  
すべての変更されたフィールドのコンテナーです。

### <a name="remarks---eventupdate"></a>備考 - eventUpdate

開発者は、特定のテーブルの更新時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventUpdate に設定することが含まれます。 レコードが更新されるとき、または特定のフィールドが更新されたときに必ず呼び出すカーネルを設定することができます。 これは、logUpdate メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、レコードが更新されたトランザクション内にあります。

## <a name="method-transactionscopebegin"></a>メソッド transactionScopeBegin

```xpp
public void transactionScopeBegin()
```

## <a name="method-checkfornewbatchjobs"></a>メソッド checkForNewBatchJobs

```xpp
public static void checkForNewBatchJobs()
```

## <a name="method-disablecountrycontextfilter"></a>メソッド disableCountryContextFilter

現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を無効にします。

```xpp
public void disableCountryContextFilter()
```

## <a name="method-xref"></a>メソッド xref

```xpp
public void xref(str path, xRef x)
```

### <a name="parameters---xref"></a>パラメーター - xref

path  

<!-- -->

x  

## <a name="method-transactionscopeabort"></a>メソッド transactionScopeAbort

```xpp
public void transactionScopeAbort()
```

## <a name="method-eventrenamekey"></a>メソッド eventRenameKey

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、主キーの名前が変更されたときにカーネルにより呼び出されるコールバックとして機能します。

```xpp
public void eventRenameKey(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---eventrenamekey"></a>パラメーター - eventRenameKey

recordOrig  
すべての変更されたフィールドのコンテナーです。

<!-- -->

recordUpdated  
すべての変更されたフィールドのコンテナーです。

<!-- -->

changedFields  
すべての変更されたフィールドのコンテナーです。

### <a name="remarks---eventrenamekey"></a>備考 - eventRenameKey

開発者は、特定のテーブルの主キーの名前の変更時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventRenameKey に設定することが含まれます。 これは、logRenameKey メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、主キーの名前が変更されたトランザクションになります。

## <a name="method-flushclientperformanceoptions"></a>メソッド flushClientPerformanceOptions

```xpp
public void flushClientPerformanceOptions()
```

## <a name="method-flushclientservices"></a>メソッド flushClientServices

```xpp
public static void flushClientServices()
```

## <a name="method-restartservicehost"></a>メソッド restartServiceHost

```xpp
public void restartServiceHost()
```

## <a name="method-updatexreftreenode"></a>メソッド updateXrefTreeNode

さまざまなノード タイプの相互参照情報が更新されると、フレームワークによって呼び出されます。

```xpp
public void updateXrefTreeNode(TreeNode treeNode)
```

### <a name="parameters---updatexreftreenode"></a>パラメーター - updateXrefTreeNode

treeNode  

### <a name="remarks---updatexreftreenode"></a>備考 - updateXrefTreeNode

Application クラスは、過負荷機能を提供します。

## <a name="method-ttscommit"></a>メソッド ttscommit

```xpp
public void ttscommit()
```

## <a name="method-requestcompanychange"></a>メソッド RequestCompanyChange

```xpp
public void RequestCompanyChange([DataAreaSysCompany company])
```

### <a name="parameters---requestcompanychange"></a>パラメーター - RequestCompanyChange

会社  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-eventinsert"></a>メソッド eventInsert

そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが挿入されたときにカーネルにより呼び出されるコールバックとして機能します。

```xpp
public void eventInsert(Common recordInserted)
```

### <a name="parameters---eventinsert"></a>パラメーター - eventInsert

recordInserted  
挿入済みレコード。

### <a name="remarks---eventinsert"></a>備考 - eventInsert

開発者は、特定のテーブルの挿入時にコール バックするカーネルを設定できます。 これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventInsert に設定することが含まれます。 これは、logInsert メソッドが呼び出されて設定される方法と非常によく似ています。 このメソッドの呼び出しは、レコードが挿入されたトランザクション内にあります。

## <a name="method-ttsnotifybegin"></a>メソッド ttsNotifyBegin

```xpp
public void ttsNotifyBegin()
```

## <a name="method-closeallforms"></a>メソッド closeAllForms

```xpp
public void closeAllForms()
```

## <a name="method-ttsnotifycommit"></a>メソッド ttsNotifyCommit

```xpp
public void ttsNotifyCommit()
```

## <a name="method-ttsnotifyprecommit"></a>メソッド ttsNotifyPreCommit

```xpp
public void ttsNotifyPreCommit()
```

## <a name="method-ttsnotifypostbegin"></a>メソッド ttsNotifyPostBegin

```xpp
public void ttsNotifyPostBegin()
```

## <a name="method-ttsnotifyabort"></a>メソッド ttsNotifyAbort

```xpp
public void ttsNotifyAbort()
```

## <a name="method-setdensity"></a>メソッド setDensity

```xpp
public void setDensity([SysUserInfoDensity theme])
```

### <a name="parameters---setdensity"></a>パラメーター - setDensity

theme  

## <a name="method-loginsert"></a>メソッド logInsert

```xpp
public void logInsert(Common recordInserted)
```

### <a name="parameters---loginsert"></a>パラメーター - logInsert

recordInserted  

