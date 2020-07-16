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
# <a name="class-xapplication"></a><span data-ttu-id="ad04b-103">クラス xApplication</span><span class="sxs-lookup"><span data-stu-id="ad04b-103">Class xApplication</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class xApplication extends Object
```

## <a name="remarks"></a><span data-ttu-id="ad04b-104">備考</span><span class="sxs-lookup"><span data-stu-id="ad04b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="ad04b-105">例</span><span class="sxs-lookup"><span data-stu-id="ad04b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ad04b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="ad04b-106">Methods</span></span>

| <span data-ttu-id="ad04b-107">方法</span><span class="sxs-lookup"><span data-stu-id="ad04b-107">Method</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="ad04b-108">説明</span><span class="sxs-lookup"><span data-stu-id="ad04b-108">Description</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad04b-109">public boolean IsTablePerHierarchyMode()</span><span class="sxs-lookup"><span data-stu-id="ad04b-109">public boolean IsTablePerHierarchyMode()</span></span>                                                                                                                                                                                            | <span data-ttu-id="ad04b-110">すべてのテーブルの継承階層をフラットにしてシステムを実行するかどうかを決定します (階層ごとの表モード)。</span><span class="sxs-lookup"><span data-stu-id="ad04b-110">Determines whether the system is being run with all table inheritance hierarchies flattened (Table per hierarchy mode).</span></span>                                                         |
| <span data-ttu-id="ad04b-111">public str buildNo()</span><span class="sxs-lookup"><span data-stu-id="ad04b-111">public str buildNo()</span></span>                                                                                                                                                                                                                |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-112">public boolean canDeleteCompany(SelectableDataArea company)</span><span class="sxs-lookup"><span data-stu-id="ad04b-112">public boolean canDeleteCompany(SelectableDataArea company)</span></span>                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-113">public int countOfTopLevelFormsOpened()</span><span class="sxs-lookup"><span data-stu-id="ad04b-113">public int countOfTopLevelFormsOpened()</span></span>                                                                                                                                                                                             |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-114">public Company company(\[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="ad04b-114">public Company company(\[SelectableDataArea company\])</span></span>                                                                                                                                                                              |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-115">public Int64 curTransactionId(\[boolean ForceTakeNumber\])</span><span class="sxs-lookup"><span data-stu-id="ad04b-115">public Int64 curTransactionId(\[boolean ForceTakeNumber\])</span></span>                                                                                                                                                                          |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-116">public boolean dbSynchronize(\[TableId tableId\], \[boolean checkAsNeeded\], \[boolean continueOnError\], \[boolean showProgress\], \[container checkSyncTables\], \[boolean createAllIndexes\], \[boolean useLockForSingleTable\])</span><span class="sxs-lookup"><span data-stu-id="ad04b-116">public boolean dbSynchronize(\[TableId tableId\], \[boolean checkAsNeeded\], \[boolean continueOnError\], \[boolean showProgress\], \[container checkSyncTables\], \[boolean createAllIndexes\], \[boolean useLockForSingleTable\])</span></span> |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-117">public str getSameNameDifferentIdFields()</span><span class="sxs-lookup"><span data-stu-id="ad04b-117">public str getSameNameDifferentIdFields()</span></span>                                                                                                                                                                                           |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-118">public Map getServiceHostStatus()</span><span class="sxs-lookup"><span data-stu-id="ad04b-118">public Map getServiceHostStatus()</span></span>                                                                                                                                                                                                   |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-119">public boolean isCheckedMode()</span><span class="sxs-lookup"><span data-stu-id="ad04b-119">public boolean isCheckedMode()</span></span>                                                                                                                                                                                                      |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-120">public boolean isConfigMode()</span><span class="sxs-lookup"><span data-stu-id="ad04b-120">public boolean isConfigMode()</span></span>                                                                                                                                                                                                       |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-121">public boolean isDemoMode()</span><span class="sxs-lookup"><span data-stu-id="ad04b-121">public boolean isDemoMode()</span></span>                                                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-122">public boolean isSqlConnected()</span><span class="sxs-lookup"><span data-stu-id="ad04b-122">public boolean isSqlConnected()</span></span>                                                                                                                                                                                                     |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-123">public int numberOfTreeNodesLoaded()</span><span class="sxs-lookup"><span data-stu-id="ad04b-123">public int numberOfTreeNodesLoaded()</span></span>                                                                                                                                                                                                |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-124">public str releaseVersion()</span><span class="sxs-lookup"><span data-stu-id="ad04b-124">public str releaseVersion()</span></span>                                                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-125">public boolean setDefaultCompany(SelectableDataArea company)</span><span class="sxs-lookup"><span data-stu-id="ad04b-125">public boolean setDefaultCompany(SelectableDataArea company)</span></span>                                                                                                                                                                        |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-126">public int ttsLevel()</span><span class="sxs-lookup"><span data-stu-id="ad04b-126">public int ttsLevel()</span></span>                                                                                                                                                                                                               |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-127">public int ttsVersion()</span><span class="sxs-lookup"><span data-stu-id="ad04b-127">public int ttsVersion()</span></span>                                                                                                                                                                                                             |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-128">::public static boolean CheckUserExistsInAnyPartition(str userId)</span><span class="sxs-lookup"><span data-stu-id="ad04b-128">::public static boolean CheckUserExistsInAnyPartition(str userId)</span></span>                                                                                                                                                                   | <span data-ttu-id="ad04b-129">指定されたユーザーがどのパーティションにも存在するかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="ad04b-129">Checks whether the given user is present in any partition.</span></span>                                                                                                                      |
| <span data-ttu-id="ad04b-130">::public static str getFolderPath(int folder)</span><span class="sxs-lookup"><span data-stu-id="ad04b-130">::public static str getFolderPath(int folder)</span></span>                                                                                                                                                                                       |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-131">::public static str getVSAssembliesPath()</span><span class="sxs-lookup"><span data-stu-id="ad04b-131">::public static str getVSAssembliesPath()</span></span>                                                                                                                                                                                           |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-132">::public static boolean ilCacheContains(str owner, str key)</span><span class="sxs-lookup"><span data-stu-id="ad04b-132">::public static boolean ilCacheContains(str owner, str key)</span></span>                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-133">::public static str ilCacheDelete(str owner, str key)</span><span class="sxs-lookup"><span data-stu-id="ad04b-133">::public static str ilCacheDelete(str owner, str key)</span></span>                                                                                                                                                                               |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-134">::public static str ilCacheFind(str owner, str key)</span><span class="sxs-lookup"><span data-stu-id="ad04b-134">::public static str ilCacheFind(str owner, str key)</span></span>                                                                                                                                                                                 |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-135">::public static boolean initPartition(Partition partition)</span><span class="sxs-lookup"><span data-stu-id="ad04b-135">::public static boolean initPartition(Partition partition)</span></span>                                                                                                                                                                          | <span data-ttu-id="ad04b-136">DAT 会社と管理者ユーザーを作成することで指定したパーティションを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-136">Initializes a given partition by creating the DAT company and the Admin user.</span></span>                                                                                                   |
| <span data-ttu-id="ad04b-137">::public static boolean isServiceRegisteredOnClient(ClassId classId)</span><span class="sxs-lookup"><span data-stu-id="ad04b-137">::public static boolean isServiceRegisteredOnClient(ClassId classId)</span></span>                                                                                                                                                                |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-138">::public static boolean IsSinglePartitionSystem()</span><span class="sxs-lookup"><span data-stu-id="ad04b-138">::public static boolean IsSinglePartitionSystem()</span></span>                                                                                                                                                                                   | <span data-ttu-id="ad04b-139">配置が単一のパーティションか複数パーティションかを評価します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-139">Evaluates whether the deployment has a single partition or multiple partitions.</span></span>                                                                                                 |
| <span data-ttu-id="ad04b-140">::public static CLRObject XppILAppDomain()</span><span class="sxs-lookup"><span data-stu-id="ad04b-140">::public static CLRObject XppILAppDomain()</span></span>                                                                                                                                                                                          |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-141">public boolean isInTransactionScope()</span><span class="sxs-lookup"><span data-stu-id="ad04b-141">public boolean isInTransactionScope()</span></span>                                                                                                                                                                                               |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-142">public Int64 transactionScopeCommitLevel()</span><span class="sxs-lookup"><span data-stu-id="ad04b-142">public Int64 transactionScopeCommitLevel()</span></span>                                                                                                                                                                                          |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-143">public container Encrypt(str input)</span><span class="sxs-lookup"><span data-stu-id="ad04b-143">public container Encrypt(str input)</span></span>                                                                                                                                                                                                 |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-144">public str Decrypt(container cipher)</span><span class="sxs-lookup"><span data-stu-id="ad04b-144">public str Decrypt(container cipher)</span></span>                                                                                                                                                                                                |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-145">public System.Security.SecureString decryptToSecureString(container cipher)</span><span class="sxs-lookup"><span data-stu-id="ad04b-145">public System.Security.SecureString decryptToSecureString(container cipher)</span></span>                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-146">public container encryptFromSecureString(System.Security.SecureString input)</span><span class="sxs-lookup"><span data-stu-id="ad04b-146">public container encryptFromSecureString(System.Security.SecureString input)</span></span>                                                                                                                                                        |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-147">public container EncryptForPurpose(str input, str purpose)</span><span class="sxs-lookup"><span data-stu-id="ad04b-147">public container EncryptForPurpose(str input, str purpose)</span></span>                                                                                                                                                                          |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-148">public str DecryptForPurpose(container cipher, str purpose)</span><span class="sxs-lookup"><span data-stu-id="ad04b-148">public str DecryptForPurpose(container cipher, str purpose)</span></span>                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-149">public System.Security.SecureString decryptToSecureStringForPurpose(container cipher, str purpose)</span><span class="sxs-lookup"><span data-stu-id="ad04b-149">public System.Security.SecureString decryptToSecureStringForPurpose(container cipher, str purpose)</span></span>                                                                                                                                  |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-150">public container encryptFromSecureStringForPurpose(System.Security.SecureString input, str purpose)</span><span class="sxs-lookup"><span data-stu-id="ad04b-150">public container encryptFromSecureStringForPurpose(System.Security.SecureString input, str purpose)</span></span>                                                                                                                                 |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-151">public str convertToUnsecureString(System.Security.SecureString secureString)</span><span class="sxs-lookup"><span data-stu-id="ad04b-151">public str convertToUnsecureString(System.Security.SecureString secureString)</span></span>                                                                                                                                                       |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-152">public System.Security.SecureString convertToSecureString(str unsecureString)</span><span class="sxs-lookup"><span data-stu-id="ad04b-152">public System.Security.SecureString convertToSecureString(str unsecureString)</span></span>                                                                                                                                                       |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-153">::public static void startBatch()</span><span class="sxs-lookup"><span data-stu-id="ad04b-153">::public static void startBatch()</span></span>                                                                                                                                                                                                   |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-154">public void deleteCompany(SelectableDataArea company)</span><span class="sxs-lookup"><span data-stu-id="ad04b-154">public void deleteCompany(SelectableDataArea company)</span></span>                                                                                                                                                                               |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-155">public void ttsabort()</span><span class="sxs-lookup"><span data-stu-id="ad04b-155">public void ttsabort()</span></span>                                                                                                                                                                                                              |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-156">public void transactionScopeCommit()</span><span class="sxs-lookup"><span data-stu-id="ad04b-156">public void transactionScopeCommit()</span></span>                                                                                                                                                                                                |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-157">public void new()</span><span class="sxs-lookup"><span data-stu-id="ad04b-157">public void new()</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="ad04b-158">xApplication クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-158">Initializes a new instance of the xApplication class.</span></span>                                                                                                                           |
| <span data-ttu-id="ad04b-159">::public static void stopBatch()</span><span class="sxs-lookup"><span data-stu-id="ad04b-159">::public static void stopBatch()</span></span>                                                                                                                                                                                                    |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-160">public void logRenameKey(Common recordOrig, Common recordUpdated, container changedFields)</span><span class="sxs-lookup"><span data-stu-id="ad04b-160">public void logRenameKey(Common recordOrig, Common recordUpdated, container changedFields)</span></span>                                                                                                                                          |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-161">public void startup(str startupCmd, str buildNumber)</span><span class="sxs-lookup"><span data-stu-id="ad04b-161">public void startup(str startupCmd, str buildNumber)</span></span>                                                                                                                                                                                |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-162">public void RedirectToDashboard()</span><span class="sxs-lookup"><span data-stu-id="ad04b-162">public void RedirectToDashboard()</span></span>                                                                                                                                                                                                   |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-163">public void insertXReferences()</span><span class="sxs-lookup"><span data-stu-id="ad04b-163">public void insertXReferences()</span></span>                                                                                                                                                                                                     | <span data-ttu-id="ad04b-164">相互参照情報をデータベースに挿入する必要があるときに、フレームワークによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-164">Is invoked by the framework when cross-reference information should be inserted into the database.</span></span>                                                                              |
| <span data-ttu-id="ad04b-165">public void logUpdate(Common recordOrig, Common recordUpdated, container changedFields)</span><span class="sxs-lookup"><span data-stu-id="ad04b-165">public void logUpdate(Common recordOrig, Common recordUpdated, container changedFields)</span></span>                                                                                                                                             |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-166">public void setStartPage(\[SysUserInfoStartPage startpage\])</span><span class="sxs-lookup"><span data-stu-id="ad04b-166">public void setStartPage(\[SysUserInfoStartPage startpage\])</span></span>                                                                                                                                                                        |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-167">::public static void ilCacheInsert(str owner, str key, str value)</span><span class="sxs-lookup"><span data-stu-id="ad04b-167">::public static void ilCacheInsert(str owner, str key, str value)</span></span>                                                                                                                                                                   |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-168">public void clearManagedCaches()</span><span class="sxs-lookup"><span data-stu-id="ad04b-168">public void clearManagedCaches()</span></span>                                                                                                                                                                                                    |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-169">public void eventDelete(Common recordDeleted)</span><span class="sxs-lookup"><span data-stu-id="ad04b-169">public void eventDelete(Common recordDeleted)</span></span>                                                                                                                                                                                       | <span data-ttu-id="ad04b-170">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが削除されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-170">Serves as a callback that is called by the kernel when a record in a table is deleted, provided that the kernel has been set up to monitor records in that table.</span></span>               |
| <span data-ttu-id="ad04b-171">public void enableCountryContextFilter()</span><span class="sxs-lookup"><span data-stu-id="ad04b-171">public void enableCountryContextFilter()</span></span>                                                                                                                                                                                            | <span data-ttu-id="ad04b-172">現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ad04b-172">Enables system-wide optimization in the data access layer, whereby fields that don't belong in the current company's country/region context are dropped from the SELECT query.</span></span>  |
| <span data-ttu-id="ad04b-173">public void setTheme(\[SysUserInfoTheme theme\])</span><span class="sxs-lookup"><span data-stu-id="ad04b-173">public void setTheme(\[SysUserInfoTheme theme\])</span></span>                                                                                                                                                                                    |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-174">public void sysTrace(SysTraceType traceType, container traceInfo)</span><span class="sxs-lookup"><span data-stu-id="ad04b-174">public void sysTrace(SysTraceType traceType, container traceInfo)</span></span>                                                                                                                                                                   |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-175">public void initGlobal(Info infoObject, VersionControl versionControlObject)</span><span class="sxs-lookup"><span data-stu-id="ad04b-175">public void initGlobal(Info infoObject, VersionControl versionControlObject)</span></span>                                                                                                                                                        |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-176">public void transactionScopeRollback(Int64 commitLevel)</span><span class="sxs-lookup"><span data-stu-id="ad04b-176">public void transactionScopeRollback(Int64 commitLevel)</span></span>                                                                                                                                                                             |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-177">public void ttsbegin()</span><span class="sxs-lookup"><span data-stu-id="ad04b-177">public void ttsbegin()</span></span>                                                                                                                                                                                                              |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-178">public void flushcompanycache(SelectableDataArea company)</span><span class="sxs-lookup"><span data-stu-id="ad04b-178">public void flushcompanycache(SelectableDataArea company)</span></span>                                                                                                                                                                           |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-179">public void logDelete(Common recordDeleted)</span><span class="sxs-lookup"><span data-stu-id="ad04b-179">public void logDelete(Common recordDeleted)</span></span>                                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-180">::public static void registerServiceOnClient(ClassId classId, str externalName)</span><span class="sxs-lookup"><span data-stu-id="ad04b-180">::public static void registerServiceOnClient(ClassId classId, str externalName)</span></span>                                                                                                                                                     |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-181">public void eventUpdate(Common recordOrig, Common recordUpdated, container changedFields)</span><span class="sxs-lookup"><span data-stu-id="ad04b-181">public void eventUpdate(Common recordOrig, Common recordUpdated, container changedFields)</span></span>                                                                                                                                           | <span data-ttu-id="ad04b-182">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが更新されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-182">Serves as a callback that is called by the kernel when a record in a table is updated, provided that the kernel has been set up to monitor records in that table.</span></span>               |
| <span data-ttu-id="ad04b-183">public void transactionScopeBegin()</span><span class="sxs-lookup"><span data-stu-id="ad04b-183">public void transactionScopeBegin()</span></span>                                                                                                                                                                                                 |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-184">::public static void checkForNewBatchJobs()</span><span class="sxs-lookup"><span data-stu-id="ad04b-184">::public static void checkForNewBatchJobs()</span></span>                                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-185">public void disableCountryContextFilter()</span><span class="sxs-lookup"><span data-stu-id="ad04b-185">public void disableCountryContextFilter()</span></span>                                                                                                                                                                                           | <span data-ttu-id="ad04b-186">現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を無効にします。</span><span class="sxs-lookup"><span data-stu-id="ad04b-186">Disables system-wide optimization in the data access layer, whereby fields that don't belong in the current company's country/region context are dropped from the SELECT query.</span></span> |
| <span data-ttu-id="ad04b-187">public void xref(str path, xRef x)</span><span class="sxs-lookup"><span data-stu-id="ad04b-187">public void xref(str path, xRef x)</span></span>                                                                                                                                                                                                  |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-188">public void transactionScopeAbort()</span><span class="sxs-lookup"><span data-stu-id="ad04b-188">public void transactionScopeAbort()</span></span>                                                                                                                                                                                                 |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-189">public void eventRenameKey(Common recordOrig, Common recordUpdated, container changedFields)</span><span class="sxs-lookup"><span data-stu-id="ad04b-189">public void eventRenameKey(Common recordOrig, Common recordUpdated, container changedFields)</span></span>                                                                                                                                        | <span data-ttu-id="ad04b-190">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、主キーの名前が変更されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-190">Serves as a callback that is called by the kernel when a primary key is renamed, provided that the kernel has been set up to monitor records in that table.</span></span>                     |
| <span data-ttu-id="ad04b-191">public void flushClientPerformanceOptions()</span><span class="sxs-lookup"><span data-stu-id="ad04b-191">public void flushClientPerformanceOptions()</span></span>                                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-192">::public static void flushClientServices()</span><span class="sxs-lookup"><span data-stu-id="ad04b-192">::public static void flushClientServices()</span></span>                                                                                                                                                                                          |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-193">public void restartServiceHost()</span><span class="sxs-lookup"><span data-stu-id="ad04b-193">public void restartServiceHost()</span></span>                                                                                                                                                                                                    |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-194">public void updateXrefTreeNode(TreeNode treeNode)</span><span class="sxs-lookup"><span data-stu-id="ad04b-194">public void updateXrefTreeNode(TreeNode treeNode)</span></span>                                                                                                                                                                                   | <span data-ttu-id="ad04b-195">さまざまなノード タイプの相互参照情報が更新されると、フレームワークによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-195">Is invoked by the framework when cross-reference information for the various node types is updated.</span></span>                                                                             |
| <span data-ttu-id="ad04b-196">public void ttscommit()</span><span class="sxs-lookup"><span data-stu-id="ad04b-196">public void ttscommit()</span></span>                                                                                                                                                                                                             |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-197">public void RequestCompanyChange(\[DataAreaSysCompany company\])</span><span class="sxs-lookup"><span data-stu-id="ad04b-197">public void RequestCompanyChange(\[DataAreaSysCompany company\])</span></span>                                                                                                                                                                    |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-198">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="ad04b-198">public void finalize()</span></span>                                                                                                                                                                                                              |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-199">public void eventInsert(Common recordInserted)</span><span class="sxs-lookup"><span data-stu-id="ad04b-199">public void eventInsert(Common recordInserted)</span></span>                                                                                                                                                                                      | <span data-ttu-id="ad04b-200">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが挿入されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-200">Serves as a callback that is called by the kernel when a record in a table is inserted, provided that the kernel has been set up to monitor records in that table.</span></span>              |
| <span data-ttu-id="ad04b-201">public void ttsNotifyBegin()</span><span class="sxs-lookup"><span data-stu-id="ad04b-201">public void ttsNotifyBegin()</span></span>                                                                                                                                                                                                        |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-202">public void closeAllForms()</span><span class="sxs-lookup"><span data-stu-id="ad04b-202">public void closeAllForms()</span></span>                                                                                                                                                                                                         |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-203">public void ttsNotifyCommit()</span><span class="sxs-lookup"><span data-stu-id="ad04b-203">public void ttsNotifyCommit()</span></span>                                                                                                                                                                                                       |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-204">public void ttsNotifyPreCommit()</span><span class="sxs-lookup"><span data-stu-id="ad04b-204">public void ttsNotifyPreCommit()</span></span>                                                                                                                                                                                                    |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-205">public void ttsNotifyPostBegin()</span><span class="sxs-lookup"><span data-stu-id="ad04b-205">public void ttsNotifyPostBegin()</span></span>                                                                                                                                                                                                    |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-206">public void ttsNotifyAbort()</span><span class="sxs-lookup"><span data-stu-id="ad04b-206">public void ttsNotifyAbort()</span></span>                                                                                                                                                                                                        |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-207">public void setDensity(\[SysUserInfoDensity theme\])</span><span class="sxs-lookup"><span data-stu-id="ad04b-207">public void setDensity(\[SysUserInfoDensity theme\])</span></span>                                                                                                                                                                                |                                                                                                                                                                                 |
| <span data-ttu-id="ad04b-208">public void logInsert(Common recordInserted)</span><span class="sxs-lookup"><span data-stu-id="ad04b-208">public void logInsert(Common recordInserted)</span></span>                                                                                                                                                                                        |                                                                                                                                                                                 |

## <a name="method-istableperhierarchymode"></a><span data-ttu-id="ad04b-209">メソッド IsTablePerHierarchyMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-209">Method IsTablePerHierarchyMode</span></span>

<span data-ttu-id="ad04b-210">すべてのテーブルの継承階層をフラットにしてシステムを実行するかどうかを決定します (階層ごとの表モード)。</span><span class="sxs-lookup"><span data-stu-id="ad04b-210">Determines whether the system is being run with all table inheritance hierarchies flattened (Table per hierarchy mode).</span></span>

```xpp
public boolean IsTablePerHierarchyMode()
```

### <a name="return-value---istableperhierarchymode"></a><span data-ttu-id="ad04b-211">戻り値 - IsTablePerHierarchyMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-211">Return Value - IsTablePerHierarchyMode</span></span>

<span data-ttu-id="ad04b-212">システムが階層別テーブル モードで実行されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ad04b-212">true if system is being run in Table per hierarchy mode; otherwise, false.</span></span>

## <a name="method-buildno"></a><span data-ttu-id="ad04b-213">メソッド buildNo</span><span class="sxs-lookup"><span data-stu-id="ad04b-213">Method buildNo</span></span>

```xpp
public str buildNo()
```

### <a name="return-value---buildno"></a><span data-ttu-id="ad04b-214">戻り値 - buildNo</span><span class="sxs-lookup"><span data-stu-id="ad04b-214">Return Value - buildNo</span></span>

## <a name="method-candeletecompany"></a><span data-ttu-id="ad04b-215">メソッド canDeleteCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-215">Method canDeleteCompany</span></span>

```xpp
public boolean canDeleteCompany(SelectableDataArea company)
```

### <a name="parameters---candeletecompany"></a><span data-ttu-id="ad04b-216">パラメーター - canDeleteCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-216">Parameters - canDeleteCompany</span></span>

<span data-ttu-id="ad04b-217">会社</span><span class="sxs-lookup"><span data-stu-id="ad04b-217">company</span></span>  

### <a name="return-value---candeletecompany"></a><span data-ttu-id="ad04b-218">戻り値 - canDeleteCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-218">Return Value - canDeleteCompany</span></span>

## <a name="method-countoftoplevelformsopened"></a><span data-ttu-id="ad04b-219">メソッド countOfTopLevelFormsOpened</span><span class="sxs-lookup"><span data-stu-id="ad04b-219">Method countOfTopLevelFormsOpened</span></span>

```xpp
public int countOfTopLevelFormsOpened()
```

### <a name="return-value---countoftoplevelformsopened"></a><span data-ttu-id="ad04b-220">戻り値 - countOfTopLevelFormsOpened</span><span class="sxs-lookup"><span data-stu-id="ad04b-220">Return Value - countOfTopLevelFormsOpened</span></span>

## <a name="method-company"></a><span data-ttu-id="ad04b-221">メソッド company</span><span class="sxs-lookup"><span data-stu-id="ad04b-221">Method company</span></span>

```xpp
public Company company([SelectableDataArea company])
```

### <a name="parameters---company"></a><span data-ttu-id="ad04b-222">パラメーター - company</span><span class="sxs-lookup"><span data-stu-id="ad04b-222">Parameters - company</span></span>

<span data-ttu-id="ad04b-223">会社</span><span class="sxs-lookup"><span data-stu-id="ad04b-223">company</span></span>  

### <a name="return-value---company"></a><span data-ttu-id="ad04b-224">戻り値 - company</span><span class="sxs-lookup"><span data-stu-id="ad04b-224">Return Value - company</span></span>

## <a name="method-curtransactionid"></a><span data-ttu-id="ad04b-225">メソッド curTransactionId</span><span class="sxs-lookup"><span data-stu-id="ad04b-225">Method curTransactionId</span></span>

```xpp
public Int64 curTransactionId([boolean ForceTakeNumber])
```

### <a name="parameters---curtransactionid"></a><span data-ttu-id="ad04b-226">パラメーター - curTransactionId</span><span class="sxs-lookup"><span data-stu-id="ad04b-226">Parameters - curTransactionId</span></span>

<span data-ttu-id="ad04b-227">ForceTakeNumber</span><span class="sxs-lookup"><span data-stu-id="ad04b-227">ForceTakeNumber</span></span>  

### <a name="return-value---curtransactionid"></a><span data-ttu-id="ad04b-228">戻り値 - curTransactionId</span><span class="sxs-lookup"><span data-stu-id="ad04b-228">Return Value - curTransactionId</span></span>

## <a name="method-dbsynchronize"></a><span data-ttu-id="ad04b-229">メソッド dbSynchronize</span><span class="sxs-lookup"><span data-stu-id="ad04b-229">Method dbSynchronize</span></span>

```xpp
public boolean dbSynchronize([TableId tableId], [boolean checkAsNeeded], [boolean continueOnError], [boolean showProgress], [container checkSyncTables], [boolean createAllIndexes], [boolean useLockForSingleTable])
```

### <a name="parameters---dbsynchronize"></a><span data-ttu-id="ad04b-230">パラメーター - dbSynchronize</span><span class="sxs-lookup"><span data-stu-id="ad04b-230">Parameters - dbSynchronize</span></span>

<span data-ttu-id="ad04b-231">tableId</span><span class="sxs-lookup"><span data-stu-id="ad04b-231">tableId</span></span>  

<!-- -->

<span data-ttu-id="ad04b-232">checkAsNeeded</span><span class="sxs-lookup"><span data-stu-id="ad04b-232">checkAsNeeded</span></span>  

<!-- -->

<span data-ttu-id="ad04b-233">continueOnError</span><span class="sxs-lookup"><span data-stu-id="ad04b-233">continueOnError</span></span>  

<!-- -->

<span data-ttu-id="ad04b-234">showProgress</span><span class="sxs-lookup"><span data-stu-id="ad04b-234">showProgress</span></span>  

<!-- -->

<span data-ttu-id="ad04b-235">checkSyncTables</span><span class="sxs-lookup"><span data-stu-id="ad04b-235">checkSyncTables</span></span>  

<!-- -->

<span data-ttu-id="ad04b-236">createAllIndexes</span><span class="sxs-lookup"><span data-stu-id="ad04b-236">createAllIndexes</span></span>  

<!-- -->

<span data-ttu-id="ad04b-237">useLockForSingleTable</span><span class="sxs-lookup"><span data-stu-id="ad04b-237">useLockForSingleTable</span></span>  

### <a name="return-value---dbsynchronize"></a><span data-ttu-id="ad04b-238">戻り値 - dbSynchronize</span><span class="sxs-lookup"><span data-stu-id="ad04b-238">Return Value - dbSynchronize</span></span>

## <a name="method-getsamenamedifferentidfields"></a><span data-ttu-id="ad04b-239">メソッド getSameNameDifferentIdFields</span><span class="sxs-lookup"><span data-stu-id="ad04b-239">Method getSameNameDifferentIdFields</span></span>

```xpp
public str getSameNameDifferentIdFields()
```

### <a name="return-value---getsamenamedifferentidfields"></a><span data-ttu-id="ad04b-240">戻り値 - getSameNameDifferentIdFields</span><span class="sxs-lookup"><span data-stu-id="ad04b-240">Return Value - getSameNameDifferentIdFields</span></span>

## <a name="method-getservicehoststatus"></a><span data-ttu-id="ad04b-241">メソッド getServiceHostStatus</span><span class="sxs-lookup"><span data-stu-id="ad04b-241">Method getServiceHostStatus</span></span>

```xpp
public Map getServiceHostStatus()
```

### <a name="return-value---getservicehoststatus"></a><span data-ttu-id="ad04b-242">戻り値 - getServiceHostStatus</span><span class="sxs-lookup"><span data-stu-id="ad04b-242">Return Value - getServiceHostStatus</span></span>

## <a name="method-ischeckedmode"></a><span data-ttu-id="ad04b-243">メソッド isCheckedMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-243">Method isCheckedMode</span></span>

```xpp
public boolean isCheckedMode()
```

### <a name="return-value---ischeckedmode"></a><span data-ttu-id="ad04b-244">戻り値 - isCheckedMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-244">Return Value - isCheckedMode</span></span>

## <a name="method-isconfigmode"></a><span data-ttu-id="ad04b-245">メソッド isConfigMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-245">Method isConfigMode</span></span>

```xpp
public boolean isConfigMode()
```

### <a name="return-value---isconfigmode"></a><span data-ttu-id="ad04b-246">戻り値 - isConfigMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-246">Return Value - isConfigMode</span></span>

## <a name="method-isdemomode"></a><span data-ttu-id="ad04b-247">メソッド isDemoMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-247">Method isDemoMode</span></span>

```xpp
public boolean isDemoMode()
```

### <a name="return-value---isdemomode"></a><span data-ttu-id="ad04b-248">戻り値 - isDemoMode</span><span class="sxs-lookup"><span data-stu-id="ad04b-248">Return Value - isDemoMode</span></span>

## <a name="method-issqlconnected"></a><span data-ttu-id="ad04b-249">メソッド isSqlConnected</span><span class="sxs-lookup"><span data-stu-id="ad04b-249">Method isSqlConnected</span></span>

```xpp
public boolean isSqlConnected()
```

### <a name="return-value---issqlconnected"></a><span data-ttu-id="ad04b-250">戻り値 - isSqlConnected</span><span class="sxs-lookup"><span data-stu-id="ad04b-250">Return Value - isSqlConnected</span></span>

## <a name="method-numberoftreenodesloaded"></a><span data-ttu-id="ad04b-251">メソッド numberOfTreeNodesLoaded</span><span class="sxs-lookup"><span data-stu-id="ad04b-251">Method numberOfTreeNodesLoaded</span></span>

```xpp
public int numberOfTreeNodesLoaded()
```

### <a name="return-value---numberoftreenodesloaded"></a><span data-ttu-id="ad04b-252">戻り値 - numberOfTreeNodesLoaded</span><span class="sxs-lookup"><span data-stu-id="ad04b-252">Return Value - numberOfTreeNodesLoaded</span></span>

## <a name="method-releaseversion"></a><span data-ttu-id="ad04b-253">メソッド releaseVersion</span><span class="sxs-lookup"><span data-stu-id="ad04b-253">Method releaseVersion</span></span>

```xpp
public str releaseVersion()
```

### <a name="return-value---releaseversion"></a><span data-ttu-id="ad04b-254">戻り値 - releaseVersion</span><span class="sxs-lookup"><span data-stu-id="ad04b-254">Return Value - releaseVersion</span></span>

## <a name="method-setdefaultcompany"></a><span data-ttu-id="ad04b-255">メソッド setDefaultCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-255">Method setDefaultCompany</span></span>

```xpp
public boolean setDefaultCompany(SelectableDataArea company)
```

### <a name="parameters---setdefaultcompany"></a><span data-ttu-id="ad04b-256">パラメーター - setDefaultCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-256">Parameters - setDefaultCompany</span></span>

<span data-ttu-id="ad04b-257">会社</span><span class="sxs-lookup"><span data-stu-id="ad04b-257">company</span></span>  

### <a name="return-value---setdefaultcompany"></a><span data-ttu-id="ad04b-258">戻り値 - setDefaultCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-258">Return Value - setDefaultCompany</span></span>

## <a name="method-ttslevel"></a><span data-ttu-id="ad04b-259">メソッド ttsLevel</span><span class="sxs-lookup"><span data-stu-id="ad04b-259">Method ttsLevel</span></span>

```xpp
public int ttsLevel()
```

### <a name="return-value---ttslevel"></a><span data-ttu-id="ad04b-260">戻り値 - ttsLevel</span><span class="sxs-lookup"><span data-stu-id="ad04b-260">Return Value - ttsLevel</span></span>

## <a name="method-ttsversion"></a><span data-ttu-id="ad04b-261">メソッド ttsVersion</span><span class="sxs-lookup"><span data-stu-id="ad04b-261">Method ttsVersion</span></span>

```xpp
public int ttsVersion()
```

### <a name="return-value---ttsversion"></a><span data-ttu-id="ad04b-262">戻り値 - ttsVersion</span><span class="sxs-lookup"><span data-stu-id="ad04b-262">Return Value - ttsVersion</span></span>

## <a name="method-checkuserexistsinanypartition"></a><span data-ttu-id="ad04b-263">メソッド CheckUserExistsInAnyPartition</span><span class="sxs-lookup"><span data-stu-id="ad04b-263">Method CheckUserExistsInAnyPartition</span></span>

<span data-ttu-id="ad04b-264">指定されたユーザーがどのパーティションにも存在するかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="ad04b-264">Checks whether the given user is present in any partition.</span></span>

```xpp
public static boolean CheckUserExistsInAnyPartition(str userId)
```

### <a name="parameters---checkuserexistsinanypartition"></a><span data-ttu-id="ad04b-265">パラメーター - CheckUserExistsInAnyPartition</span><span class="sxs-lookup"><span data-stu-id="ad04b-265">Parameters - CheckUserExistsInAnyPartition</span></span>

<span data-ttu-id="ad04b-266">userId</span><span class="sxs-lookup"><span data-stu-id="ad04b-266">userId</span></span>  

### <a name="return-value---checkuserexistsinanypartition"></a><span data-ttu-id="ad04b-267">戻り値 - CheckUserExistsInAnyPartition</span><span class="sxs-lookup"><span data-stu-id="ad04b-267">Return Value - CheckUserExistsInAnyPartition</span></span>

<span data-ttu-id="ad04b-268">ユーザーがいずれかのパーティションに存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ad04b-268">true if the user exists in any of the partitions; otherwise, false.</span></span>

## <a name="method-getfolderpath"></a><span data-ttu-id="ad04b-269">メソッド getFolderPath</span><span class="sxs-lookup"><span data-stu-id="ad04b-269">Method getFolderPath</span></span>

```xpp
public static str getFolderPath(int folder)
```

### <a name="parameters---getfolderpath"></a><span data-ttu-id="ad04b-270">パラメーター - getFolderPath</span><span class="sxs-lookup"><span data-stu-id="ad04b-270">Parameters - getFolderPath</span></span>

<span data-ttu-id="ad04b-271">folder</span><span class="sxs-lookup"><span data-stu-id="ad04b-271">folder</span></span>  

### <a name="return-value---getfolderpath"></a><span data-ttu-id="ad04b-272">戻り値 - getFolderPath</span><span class="sxs-lookup"><span data-stu-id="ad04b-272">Return Value - getFolderPath</span></span>

## <a name="method-getvsassembliespath"></a><span data-ttu-id="ad04b-273">メソッド getVSAssembliesPath</span><span class="sxs-lookup"><span data-stu-id="ad04b-273">Method getVSAssembliesPath</span></span>

```xpp
public static str getVSAssembliesPath()
```

### <a name="return-value---getvsassembliespath"></a><span data-ttu-id="ad04b-274">戻り値 - getVSAssembliesPath</span><span class="sxs-lookup"><span data-stu-id="ad04b-274">Return Value - getVSAssembliesPath</span></span>

## <a name="method-ilcachecontains"></a><span data-ttu-id="ad04b-275">メソッド ilCacheContains</span><span class="sxs-lookup"><span data-stu-id="ad04b-275">Method ilCacheContains</span></span>

```xpp
public static boolean ilCacheContains(str owner, str key)
```

### <a name="parameters---ilcachecontains"></a><span data-ttu-id="ad04b-276">パラメーター - ilCacheContains</span><span class="sxs-lookup"><span data-stu-id="ad04b-276">Parameters - ilCacheContains</span></span>

<span data-ttu-id="ad04b-277">所有者</span><span class="sxs-lookup"><span data-stu-id="ad04b-277">owner</span></span>  

<!-- -->

<span data-ttu-id="ad04b-278">キー</span><span class="sxs-lookup"><span data-stu-id="ad04b-278">key</span></span>  

### <a name="return-value---ilcachecontains"></a><span data-ttu-id="ad04b-279">戻り値 - ilCacheContains</span><span class="sxs-lookup"><span data-stu-id="ad04b-279">Return Value - ilCacheContains</span></span>

## <a name="method-ilcachedelete"></a><span data-ttu-id="ad04b-280">メソッド ilCacheDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-280">Method ilCacheDelete</span></span>

```xpp
public static str ilCacheDelete(str owner, str key)
```

### <a name="parameters---ilcachedelete"></a><span data-ttu-id="ad04b-281">パラメーター - ilCacheDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-281">Parameters - ilCacheDelete</span></span>

<span data-ttu-id="ad04b-282">所有者</span><span class="sxs-lookup"><span data-stu-id="ad04b-282">owner</span></span>  

<!-- -->

<span data-ttu-id="ad04b-283">キー</span><span class="sxs-lookup"><span data-stu-id="ad04b-283">key</span></span>  

### <a name="return-value---ilcachedelete"></a><span data-ttu-id="ad04b-284">戻り値 - ilCacheDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-284">Return Value - ilCacheDelete</span></span>

## <a name="method-ilcachefind"></a><span data-ttu-id="ad04b-285">メソッド ilCacheFind</span><span class="sxs-lookup"><span data-stu-id="ad04b-285">Method ilCacheFind</span></span>

```xpp
public static str ilCacheFind(str owner, str key)
```

### <a name="parameters---ilcachefind"></a><span data-ttu-id="ad04b-286">パラメーター - ilCacheFind</span><span class="sxs-lookup"><span data-stu-id="ad04b-286">Parameters - ilCacheFind</span></span>

<span data-ttu-id="ad04b-287">所有者</span><span class="sxs-lookup"><span data-stu-id="ad04b-287">owner</span></span>  

<!-- -->

<span data-ttu-id="ad04b-288">キー</span><span class="sxs-lookup"><span data-stu-id="ad04b-288">key</span></span>  

### <a name="return-value---ilcachefind"></a><span data-ttu-id="ad04b-289">戻り値 - ilCacheFind</span><span class="sxs-lookup"><span data-stu-id="ad04b-289">Return Value - ilCacheFind</span></span>

## <a name="method-initpartition"></a><span data-ttu-id="ad04b-290">メソッド initPartition</span><span class="sxs-lookup"><span data-stu-id="ad04b-290">Method initPartition</span></span>

<span data-ttu-id="ad04b-291">DAT 会社と管理者ユーザーを作成することで指定したパーティションを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-291">Initializes a given partition by creating the DAT company and the Admin user.</span></span>

```xpp
public static boolean initPartition(Partition partition)
```

### <a name="parameters---initpartition"></a><span data-ttu-id="ad04b-292">パラメーター - initPartition</span><span class="sxs-lookup"><span data-stu-id="ad04b-292">Parameters - initPartition</span></span>

<span data-ttu-id="ad04b-293">パーティション</span><span class="sxs-lookup"><span data-stu-id="ad04b-293">partition</span></span>  
<span data-ttu-id="ad04b-294">初期化するパーティションのレコード ID。</span><span class="sxs-lookup"><span data-stu-id="ad04b-294">The record ID of the partition to initialize.</span></span>

### <a name="return-value---initpartition"></a><span data-ttu-id="ad04b-295">戻り値 - initPartition</span><span class="sxs-lookup"><span data-stu-id="ad04b-295">Return Value - initPartition</span></span>

<span data-ttu-id="ad04b-296">初期化が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ad04b-296">true if the initialization is successful; otherwise, false.</span></span>

### <a name="remarks---initpartition"></a><span data-ttu-id="ad04b-297">備考 - initPartition</span><span class="sxs-lookup"><span data-stu-id="ad04b-297">Remarks - initPartition</span></span>

<span data-ttu-id="ad04b-298">この API は、アップグレード フレームワークでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-298">This API is meant only for use by the upgrade framework.</span></span> <span data-ttu-id="ad04b-299">それを他のコンテキストで使用すると、データに回復不能な影響が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="ad04b-299">Using it in other contexts could cause unrecoverable impact to data.</span></span>

## <a name="method-isserviceregisteredonclient"></a><span data-ttu-id="ad04b-300">メソッド isServiceRegisteredOnClient</span><span class="sxs-lookup"><span data-stu-id="ad04b-300">Method isServiceRegisteredOnClient</span></span>

```xpp
public static boolean isServiceRegisteredOnClient(ClassId classId)
```

### <a name="parameters---isserviceregisteredonclient"></a><span data-ttu-id="ad04b-301">パラメーター - isServiceRegisteredOnClient</span><span class="sxs-lookup"><span data-stu-id="ad04b-301">Parameters - isServiceRegisteredOnClient</span></span>

<span data-ttu-id="ad04b-302">classId</span><span class="sxs-lookup"><span data-stu-id="ad04b-302">classId</span></span>  

### <a name="return-value---isserviceregisteredonclient"></a><span data-ttu-id="ad04b-303">戻り値 - isServiceRegisteredOnClient</span><span class="sxs-lookup"><span data-stu-id="ad04b-303">Return Value - isServiceRegisteredOnClient</span></span>

## <a name="method-issinglepartitionsystem"></a><span data-ttu-id="ad04b-304">メソッド IsSinglePartitionSystem</span><span class="sxs-lookup"><span data-stu-id="ad04b-304">Method IsSinglePartitionSystem</span></span>

<span data-ttu-id="ad04b-305">配置が単一のパーティションか複数パーティションかを評価します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-305">Evaluates whether the deployment has a single partition or multiple partitions.</span></span>

```xpp
public static boolean IsSinglePartitionSystem()
```

### <a name="return-value---issinglepartitionsystem"></a><span data-ttu-id="ad04b-306">戻り値 - IsSinglePartitionSystem</span><span class="sxs-lookup"><span data-stu-id="ad04b-306">Return Value - IsSinglePartitionSystem</span></span>

<span data-ttu-id="ad04b-307">展開にパーティションが 1 つのみある場合は true。展開に複数のパーティションがある場合は false。</span><span class="sxs-lookup"><span data-stu-id="ad04b-307">true if the deployment has only one partition; false if the deployment has multiple partitions.</span></span>

## <a name="method-xppilappdomain"></a><span data-ttu-id="ad04b-308">メソッド XppILAppDomain</span><span class="sxs-lookup"><span data-stu-id="ad04b-308">Method XppILAppDomain</span></span>

```xpp
public static CLRObject XppILAppDomain()
```

### <a name="return-value---xppilappdomain"></a><span data-ttu-id="ad04b-309">戻り値 - XppILAppDomain</span><span class="sxs-lookup"><span data-stu-id="ad04b-309">Return Value - XppILAppDomain</span></span>

## <a name="method-isintransactionscope"></a><span data-ttu-id="ad04b-310">メソッド isInTransactionScope</span><span class="sxs-lookup"><span data-stu-id="ad04b-310">Method isInTransactionScope</span></span>

```xpp
public boolean isInTransactionScope()
```

### <a name="return-value---isintransactionscope"></a><span data-ttu-id="ad04b-311">戻り値 - isInTransactionScope</span><span class="sxs-lookup"><span data-stu-id="ad04b-311">Return Value - isInTransactionScope</span></span>

## <a name="method-transactionscopecommitlevel"></a><span data-ttu-id="ad04b-312">メソッド transactionScopeCommitLevel</span><span class="sxs-lookup"><span data-stu-id="ad04b-312">Method transactionScopeCommitLevel</span></span>

```xpp
public Int64 transactionScopeCommitLevel()
```

### <a name="return-value---transactionscopecommitlevel"></a><span data-ttu-id="ad04b-313">戻り値 - transactionScopeCommitLevel</span><span class="sxs-lookup"><span data-stu-id="ad04b-313">Return Value - transactionScopeCommitLevel</span></span>

## <a name="method-encrypt"></a><span data-ttu-id="ad04b-314">メソッド Encrypt</span><span class="sxs-lookup"><span data-stu-id="ad04b-314">Method Encrypt</span></span>

```xpp
public container Encrypt(str input)
```

### <a name="parameters---encrypt"></a><span data-ttu-id="ad04b-315">パラメーター - Encrypt</span><span class="sxs-lookup"><span data-stu-id="ad04b-315">Parameters - Encrypt</span></span>

<span data-ttu-id="ad04b-316">入力</span><span class="sxs-lookup"><span data-stu-id="ad04b-316">input</span></span>  

### <a name="return-value---encrypt"></a><span data-ttu-id="ad04b-317">戻り値 - Encrypt</span><span class="sxs-lookup"><span data-stu-id="ad04b-317">Return Value - Encrypt</span></span>

## <a name="method-decrypt"></a><span data-ttu-id="ad04b-318">メソッド Decrypt</span><span class="sxs-lookup"><span data-stu-id="ad04b-318">Method Decrypt</span></span>

```xpp
public str Decrypt(container cipher)
```

### <a name="parameters---decrypt"></a><span data-ttu-id="ad04b-319">パラメーター - Decrypt</span><span class="sxs-lookup"><span data-stu-id="ad04b-319">Parameters - Decrypt</span></span>

<span data-ttu-id="ad04b-320">cipher</span><span class="sxs-lookup"><span data-stu-id="ad04b-320">cipher</span></span>  

### <a name="return-value---decrypt"></a><span data-ttu-id="ad04b-321">戻り値 - Decrypt</span><span class="sxs-lookup"><span data-stu-id="ad04b-321">Return Value - Decrypt</span></span>

## <a name="method-decrypttosecurestring"></a><span data-ttu-id="ad04b-322">メソッド decryptToSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-322">Method decryptToSecureString</span></span>

```xpp
public System.Security.SecureString decryptToSecureString(container cipher)
```

### <a name="parameters---decrypttosecurestring"></a><span data-ttu-id="ad04b-323">パラメーター - decryptToSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-323">Parameters - decryptToSecureString</span></span>

<span data-ttu-id="ad04b-324">cipher</span><span class="sxs-lookup"><span data-stu-id="ad04b-324">cipher</span></span>  

### <a name="return-value---decrypttosecurestring"></a><span data-ttu-id="ad04b-325">戻り値 - decryptToSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-325">Return Value - decryptToSecureString</span></span>

## <a name="method-encryptfromsecurestring"></a><span data-ttu-id="ad04b-326">メソッド encryptFromSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-326">Method encryptFromSecureString</span></span>

```xpp
public container encryptFromSecureString(System.Security.SecureString input)
```

### <a name="parameters---encryptfromsecurestring"></a><span data-ttu-id="ad04b-327">パラメーター - encryptFromSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-327">Parameters - encryptFromSecureString</span></span>

<span data-ttu-id="ad04b-328">入力</span><span class="sxs-lookup"><span data-stu-id="ad04b-328">input</span></span>  

### <a name="return-value---encryptfromsecurestring"></a><span data-ttu-id="ad04b-329">戻り値 - encryptFromSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-329">Return Value - encryptFromSecureString</span></span>

## <a name="method-encryptforpurpose"></a><span data-ttu-id="ad04b-330">メソッド EncryptForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-330">Method EncryptForPurpose</span></span>

```xpp
public container EncryptForPurpose(str input, str purpose)
```

### <a name="parameters---encryptforpurpose"></a><span data-ttu-id="ad04b-331">パラメーター - EncryptForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-331">Parameters - EncryptForPurpose</span></span>

<span data-ttu-id="ad04b-332">入力</span><span class="sxs-lookup"><span data-stu-id="ad04b-332">input</span></span>  

<!-- -->

<span data-ttu-id="ad04b-333">purpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-333">purpose</span></span>  

### <a name="return-value---encryptforpurpose"></a><span data-ttu-id="ad04b-334">戻り値 - EncryptForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-334">Return Value - EncryptForPurpose</span></span>

## <a name="method-decryptforpurpose"></a><span data-ttu-id="ad04b-335">メソッド DecryptForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-335">Method DecryptForPurpose</span></span>

```xpp
public str DecryptForPurpose(container cipher, str purpose)
```

### <a name="parameters---decryptforpurpose"></a><span data-ttu-id="ad04b-336">パラメーター - DecryptForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-336">Parameters - DecryptForPurpose</span></span>

<span data-ttu-id="ad04b-337">cipher</span><span class="sxs-lookup"><span data-stu-id="ad04b-337">cipher</span></span>  

<!-- -->

<span data-ttu-id="ad04b-338">purpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-338">purpose</span></span>  

### <a name="return-value---decryptforpurpose"></a><span data-ttu-id="ad04b-339">戻り値 - DecryptForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-339">Return Value - DecryptForPurpose</span></span>

## <a name="method-decrypttosecurestringforpurpose"></a><span data-ttu-id="ad04b-340">メソッド decryptToSecureStringForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-340">Method decryptToSecureStringForPurpose</span></span>

```xpp
public System.Security.SecureString decryptToSecureStringForPurpose(container cipher, str purpose)
```

### <a name="parameters---decrypttosecurestringforpurpose"></a><span data-ttu-id="ad04b-341">パラメーター - decryptToSecureStringForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-341">Parameters - decryptToSecureStringForPurpose</span></span>

<span data-ttu-id="ad04b-342">cipher</span><span class="sxs-lookup"><span data-stu-id="ad04b-342">cipher</span></span>  

<!-- -->

<span data-ttu-id="ad04b-343">purpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-343">purpose</span></span>  

### <a name="return-value---decrypttosecurestringforpurpose"></a><span data-ttu-id="ad04b-344">戻り値 - decryptToSecureStringForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-344">Return Value - decryptToSecureStringForPurpose</span></span>

## <a name="method-encryptfromsecurestringforpurpose"></a><span data-ttu-id="ad04b-345">メソッド encryptFromSecureStringForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-345">Method encryptFromSecureStringForPurpose</span></span>

```xpp
public container encryptFromSecureStringForPurpose(System.Security.SecureString input, str purpose)
```

### <a name="parameters---encryptfromsecurestringforpurpose"></a><span data-ttu-id="ad04b-346">パラメーター - encryptFromSecureStringForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-346">Parameters - encryptFromSecureStringForPurpose</span></span>

<span data-ttu-id="ad04b-347">入力</span><span class="sxs-lookup"><span data-stu-id="ad04b-347">input</span></span>  

<!-- -->

<span data-ttu-id="ad04b-348">purpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-348">purpose</span></span>  

### <a name="return-value---encryptfromsecurestringforpurpose"></a><span data-ttu-id="ad04b-349">戻り値 - encryptFromSecureStringForPurpose</span><span class="sxs-lookup"><span data-stu-id="ad04b-349">Return Value - encryptFromSecureStringForPurpose</span></span>

## <a name="method-converttounsecurestring"></a><span data-ttu-id="ad04b-350">メソッド convertToUnsecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-350">Method convertToUnsecureString</span></span>

```xpp
public str convertToUnsecureString(System.Security.SecureString secureString)
```

### <a name="parameters---converttounsecurestring"></a><span data-ttu-id="ad04b-351">パラメーター - convertToUnsecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-351">Parameters - convertToUnsecureString</span></span>

<span data-ttu-id="ad04b-352">secureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-352">secureString</span></span>  

### <a name="return-value---converttounsecurestring"></a><span data-ttu-id="ad04b-353">戻り値 - convertToUnsecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-353">Return Value - convertToUnsecureString</span></span>

## <a name="method-converttosecurestring"></a><span data-ttu-id="ad04b-354">メソッド convertToSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-354">Method convertToSecureString</span></span>

```xpp
public System.Security.SecureString convertToSecureString(str unsecureString)
```

### <a name="parameters---converttosecurestring"></a><span data-ttu-id="ad04b-355">パラメーター - convertToSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-355">Parameters - convertToSecureString</span></span>

<span data-ttu-id="ad04b-356">unsecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-356">unsecureString</span></span>  

### <a name="return-value---converttosecurestring"></a><span data-ttu-id="ad04b-357">戻り値 - convertToSecureString</span><span class="sxs-lookup"><span data-stu-id="ad04b-357">Return Value - convertToSecureString</span></span>

## <a name="method-startbatch"></a><span data-ttu-id="ad04b-358">メソッド startBatch</span><span class="sxs-lookup"><span data-stu-id="ad04b-358">Method startBatch</span></span>

```xpp
public static void startBatch()
```

## <a name="method-deletecompany"></a><span data-ttu-id="ad04b-359">メソッド deleteCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-359">Method deleteCompany</span></span>

```xpp
public void deleteCompany(SelectableDataArea company)
```

### <a name="parameters---deletecompany"></a><span data-ttu-id="ad04b-360">パラメーター - deleteCompany</span><span class="sxs-lookup"><span data-stu-id="ad04b-360">Parameters - deleteCompany</span></span>

<span data-ttu-id="ad04b-361">会社</span><span class="sxs-lookup"><span data-stu-id="ad04b-361">company</span></span>  

## <a name="method-ttsabort"></a><span data-ttu-id="ad04b-362">メソッド ttsabort</span><span class="sxs-lookup"><span data-stu-id="ad04b-362">Method ttsabort</span></span>

```xpp
public void ttsabort()
```

## <a name="method-transactionscopecommit"></a><span data-ttu-id="ad04b-363">メソッド transactionScopeCommit</span><span class="sxs-lookup"><span data-stu-id="ad04b-363">Method transactionScopeCommit</span></span>

```xpp
public void transactionScopeCommit()
```

## <a name="method-new"></a><span data-ttu-id="ad04b-364">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ad04b-364">Method new</span></span>

<span data-ttu-id="ad04b-365">xApplication クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-365">Initializes a new instance of the xApplication class.</span></span>

```xpp
public void new()
```

## <a name="method-stopbatch"></a><span data-ttu-id="ad04b-366">メソッド stopBatch</span><span class="sxs-lookup"><span data-stu-id="ad04b-366">Method stopBatch</span></span>

```xpp
public static void stopBatch()
```

## <a name="method-logrenamekey"></a><span data-ttu-id="ad04b-367">メソッド logRenameKey</span><span class="sxs-lookup"><span data-stu-id="ad04b-367">Method logRenameKey</span></span>

```xpp
public void logRenameKey(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---logrenamekey"></a><span data-ttu-id="ad04b-368">パラメーター - logRenameKey</span><span class="sxs-lookup"><span data-stu-id="ad04b-368">Parameters - logRenameKey</span></span>

<span data-ttu-id="ad04b-369">recordOrig</span><span class="sxs-lookup"><span data-stu-id="ad04b-369">recordOrig</span></span>  

<!-- -->

<span data-ttu-id="ad04b-370">recordUpdated</span><span class="sxs-lookup"><span data-stu-id="ad04b-370">recordUpdated</span></span>  

<!-- -->

<span data-ttu-id="ad04b-371">changedFields</span><span class="sxs-lookup"><span data-stu-id="ad04b-371">changedFields</span></span>  

## <a name="method-startup"></a><span data-ttu-id="ad04b-372">メソッド startup</span><span class="sxs-lookup"><span data-stu-id="ad04b-372">Method startup</span></span>

```xpp
public void startup(str startupCmd, str buildNumber)
```

### <a name="parameters---startup"></a><span data-ttu-id="ad04b-373">パラメーター - startup</span><span class="sxs-lookup"><span data-stu-id="ad04b-373">Parameters - startup</span></span>

<span data-ttu-id="ad04b-374">startupCmd</span><span class="sxs-lookup"><span data-stu-id="ad04b-374">startupCmd</span></span>  

<!-- -->

<span data-ttu-id="ad04b-375">buildNumber</span><span class="sxs-lookup"><span data-stu-id="ad04b-375">buildNumber</span></span>  

## <a name="method-redirecttodashboard"></a><span data-ttu-id="ad04b-376">メソッド RedirectToDashboard</span><span class="sxs-lookup"><span data-stu-id="ad04b-376">Method RedirectToDashboard</span></span>

```xpp
public void RedirectToDashboard()
```

## <a name="method-insertxreferences"></a><span data-ttu-id="ad04b-377">メソッド insertXReferences</span><span class="sxs-lookup"><span data-stu-id="ad04b-377">Method insertXReferences</span></span>

<span data-ttu-id="ad04b-378">相互参照情報をデータベースに挿入する必要があるときに、フレームワークによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-378">Is invoked by the framework when cross-reference information should be inserted into the database.</span></span>

```xpp
public void insertXReferences()
```

### <a name="remarks---insertxreferences"></a><span data-ttu-id="ad04b-379">備考 - insertXReferences</span><span class="sxs-lookup"><span data-stu-id="ad04b-379">Remarks - insertXReferences</span></span>

<span data-ttu-id="ad04b-380">Application クラスは、過負荷機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-380">The Application class provides the overloaded functionality.</span></span>

## <a name="method-logupdate"></a><span data-ttu-id="ad04b-381">メソッド logUpdate</span><span class="sxs-lookup"><span data-stu-id="ad04b-381">Method logUpdate</span></span>

```xpp
public void logUpdate(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---logupdate"></a><span data-ttu-id="ad04b-382">パラメーター - logUpdate</span><span class="sxs-lookup"><span data-stu-id="ad04b-382">Parameters - logUpdate</span></span>

<span data-ttu-id="ad04b-383">recordOrig</span><span class="sxs-lookup"><span data-stu-id="ad04b-383">recordOrig</span></span>  

<!-- -->

<span data-ttu-id="ad04b-384">recordUpdated</span><span class="sxs-lookup"><span data-stu-id="ad04b-384">recordUpdated</span></span>  

<!-- -->

<span data-ttu-id="ad04b-385">changedFields</span><span class="sxs-lookup"><span data-stu-id="ad04b-385">changedFields</span></span>  

## <a name="method-setstartpage"></a><span data-ttu-id="ad04b-386">メソッド setStartPage</span><span class="sxs-lookup"><span data-stu-id="ad04b-386">Method setStartPage</span></span>

```xpp
public void setStartPage([SysUserInfoStartPage startpage])
```

### <a name="parameters---setstartpage"></a><span data-ttu-id="ad04b-387">パラメーター - setStartPage</span><span class="sxs-lookup"><span data-stu-id="ad04b-387">Parameters - setStartPage</span></span>

<span data-ttu-id="ad04b-388">startpage</span><span class="sxs-lookup"><span data-stu-id="ad04b-388">startpage</span></span>  

## <a name="method-ilcacheinsert"></a><span data-ttu-id="ad04b-389">メソッド ilCacheInsert</span><span class="sxs-lookup"><span data-stu-id="ad04b-389">Method ilCacheInsert</span></span>

```xpp
public static void ilCacheInsert(str owner, str key, str value)
```

### <a name="parameters---ilcacheinsert"></a><span data-ttu-id="ad04b-390">パラメーター - ilCacheInsert</span><span class="sxs-lookup"><span data-stu-id="ad04b-390">Parameters - ilCacheInsert</span></span>

<span data-ttu-id="ad04b-391">所有者</span><span class="sxs-lookup"><span data-stu-id="ad04b-391">owner</span></span>  

<!-- -->

<span data-ttu-id="ad04b-392">キー</span><span class="sxs-lookup"><span data-stu-id="ad04b-392">key</span></span>  

<!-- -->

<span data-ttu-id="ad04b-393">値</span><span class="sxs-lookup"><span data-stu-id="ad04b-393">value</span></span>  

## <a name="method-clearmanagedcaches"></a><span data-ttu-id="ad04b-394">メソッド clearManagedCaches</span><span class="sxs-lookup"><span data-stu-id="ad04b-394">Method clearManagedCaches</span></span>

```xpp
public void clearManagedCaches()
```

## <a name="method-eventdelete"></a><span data-ttu-id="ad04b-395">メソッド eventDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-395">Method eventDelete</span></span>

<span data-ttu-id="ad04b-396">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが削除されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-396">Serves as a callback that is called by the kernel when a record in a table is deleted, provided that the kernel has been set up to monitor records in that table.</span></span>

```xpp
public void eventDelete(Common recordDeleted)
```

### <a name="parameters---eventdelete"></a><span data-ttu-id="ad04b-397">パラメーター - eventDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-397">Parameters - eventDelete</span></span>

<span data-ttu-id="ad04b-398">recordDeleted</span><span class="sxs-lookup"><span data-stu-id="ad04b-398">recordDeleted</span></span>  
<span data-ttu-id="ad04b-399">削除したレコード。</span><span class="sxs-lookup"><span data-stu-id="ad04b-399">The deleted record.</span></span>

### <a name="remarks---eventdelete"></a><span data-ttu-id="ad04b-400">備考 - eventDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-400">Remarks - eventDelete</span></span>

<span data-ttu-id="ad04b-401">開発者は、特定のテーブルの削除時にコール バックするカーネルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-401">A developer can set up the kernel to call back on deletes for a given table.</span></span> <span data-ttu-id="ad04b-402">これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実現できます。これには、logType フィールドを EventDelete に設定することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-402">This can be accomplished by inserting a record into the DatabaseLog kernel table with all fields set to relevant values, which includes setting the field logType to EventDelete.</span></span> <span data-ttu-id="ad04b-403">これは、logDelete メソッドが呼び出されて設定される方法と非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="ad04b-403">This is very similar to how the logDelete method is called and set up.</span></span> <span data-ttu-id="ad04b-404">このメソッドの呼び出しは、レコードが削除されたトランザクション内にあります。</span><span class="sxs-lookup"><span data-stu-id="ad04b-404">The call of this method will be in the transaction in which the record is deleted.</span></span>

## <a name="method-enablecountrycontextfilter"></a><span data-ttu-id="ad04b-405">メソッド enableCountryContextFilter</span><span class="sxs-lookup"><span data-stu-id="ad04b-405">Method enableCountryContextFilter</span></span>

<span data-ttu-id="ad04b-406">現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ad04b-406">Enables system-wide optimization in the data access layer, whereby fields that don't belong in the current company's country/region context are dropped from the SELECT query.</span></span>

```xpp
public void enableCountryContextFilter()
```

## <a name="method-settheme"></a><span data-ttu-id="ad04b-407">メソッド setTheme</span><span class="sxs-lookup"><span data-stu-id="ad04b-407">Method setTheme</span></span>

```xpp
public void setTheme([SysUserInfoTheme theme])
```

### <a name="parameters---settheme"></a><span data-ttu-id="ad04b-408">パラメーター - setTheme</span><span class="sxs-lookup"><span data-stu-id="ad04b-408">Parameters - setTheme</span></span>

<span data-ttu-id="ad04b-409">theme</span><span class="sxs-lookup"><span data-stu-id="ad04b-409">theme</span></span>  

## <a name="method-systrace"></a><span data-ttu-id="ad04b-410">メソッド sysTrace</span><span class="sxs-lookup"><span data-stu-id="ad04b-410">Method sysTrace</span></span>

```xpp
public void sysTrace(SysTraceType traceType, container traceInfo)
```

### <a name="parameters---systrace"></a><span data-ttu-id="ad04b-411">パラメーター - sysTrace</span><span class="sxs-lookup"><span data-stu-id="ad04b-411">Parameters - sysTrace</span></span>

<span data-ttu-id="ad04b-412">traceType</span><span class="sxs-lookup"><span data-stu-id="ad04b-412">traceType</span></span>  

<!-- -->

<span data-ttu-id="ad04b-413">traceInfo</span><span class="sxs-lookup"><span data-stu-id="ad04b-413">traceInfo</span></span>  

## <a name="method-initglobal"></a><span data-ttu-id="ad04b-414">メソッド initGlobal</span><span class="sxs-lookup"><span data-stu-id="ad04b-414">Method initGlobal</span></span>

```xpp
public void initGlobal(Info infoObject, VersionControl versionControlObject)
```

### <a name="parameters---initglobal"></a><span data-ttu-id="ad04b-415">パラメーター - initGlobal</span><span class="sxs-lookup"><span data-stu-id="ad04b-415">Parameters - initGlobal</span></span>

<span data-ttu-id="ad04b-416">infoObject</span><span class="sxs-lookup"><span data-stu-id="ad04b-416">infoObject</span></span>  

<!-- -->

<span data-ttu-id="ad04b-417">versionControlObject</span><span class="sxs-lookup"><span data-stu-id="ad04b-417">versionControlObject</span></span>  

## <a name="method-transactionscoperollback"></a><span data-ttu-id="ad04b-418">メソッド transactionScopeRollback</span><span class="sxs-lookup"><span data-stu-id="ad04b-418">Method transactionScopeRollback</span></span>

```xpp
public void transactionScopeRollback(Int64 commitLevel)
```

### <a name="parameters---transactionscoperollback"></a><span data-ttu-id="ad04b-419">パラメーター - transactionScopeRollback</span><span class="sxs-lookup"><span data-stu-id="ad04b-419">Parameters - transactionScopeRollback</span></span>

<span data-ttu-id="ad04b-420">commitLevel</span><span class="sxs-lookup"><span data-stu-id="ad04b-420">commitLevel</span></span>  

## <a name="method-ttsbegin"></a><span data-ttu-id="ad04b-421">メソッド ttsbegin</span><span class="sxs-lookup"><span data-stu-id="ad04b-421">Method ttsbegin</span></span>

```xpp
public void ttsbegin()
```

## <a name="method-flushcompanycache"></a><span data-ttu-id="ad04b-422">メソッド flushcompanycache</span><span class="sxs-lookup"><span data-stu-id="ad04b-422">Method flushcompanycache</span></span>

```xpp
public void flushcompanycache(SelectableDataArea company)
```

### <a name="parameters---flushcompanycache"></a><span data-ttu-id="ad04b-423">パラメーター - flushcompanycache</span><span class="sxs-lookup"><span data-stu-id="ad04b-423">Parameters - flushcompanycache</span></span>

<span data-ttu-id="ad04b-424">会社</span><span class="sxs-lookup"><span data-stu-id="ad04b-424">company</span></span>  

## <a name="method-logdelete"></a><span data-ttu-id="ad04b-425">メソッド logDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-425">Method logDelete</span></span>

```xpp
public void logDelete(Common recordDeleted)
```

### <a name="parameters---logdelete"></a><span data-ttu-id="ad04b-426">パラメーター - logDelete</span><span class="sxs-lookup"><span data-stu-id="ad04b-426">Parameters - logDelete</span></span>

<span data-ttu-id="ad04b-427">recordDeleted</span><span class="sxs-lookup"><span data-stu-id="ad04b-427">recordDeleted</span></span>  

## <a name="method-registerserviceonclient"></a><span data-ttu-id="ad04b-428">メソッド registerServiceOnClient</span><span class="sxs-lookup"><span data-stu-id="ad04b-428">Method registerServiceOnClient</span></span>

```xpp
public static void registerServiceOnClient(ClassId classId, str externalName)
```

### <a name="parameters---registerserviceonclient"></a><span data-ttu-id="ad04b-429">パラメーター - registerServiceOnClient</span><span class="sxs-lookup"><span data-stu-id="ad04b-429">Parameters - registerServiceOnClient</span></span>

<span data-ttu-id="ad04b-430">classId</span><span class="sxs-lookup"><span data-stu-id="ad04b-430">classId</span></span>  

<!-- -->

<span data-ttu-id="ad04b-431">externalName</span><span class="sxs-lookup"><span data-stu-id="ad04b-431">externalName</span></span>  

## <a name="method-eventupdate"></a><span data-ttu-id="ad04b-432">メソッド eventUpdate</span><span class="sxs-lookup"><span data-stu-id="ad04b-432">Method eventUpdate</span></span>

<span data-ttu-id="ad04b-433">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが更新されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-433">Serves as a callback that is called by the kernel when a record in a table is updated, provided that the kernel has been set up to monitor records in that table.</span></span>

```xpp
public void eventUpdate(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---eventupdate"></a><span data-ttu-id="ad04b-434">パラメーター - eventUpdate</span><span class="sxs-lookup"><span data-stu-id="ad04b-434">Parameters - eventUpdate</span></span>

<span data-ttu-id="ad04b-435">recordOrig</span><span class="sxs-lookup"><span data-stu-id="ad04b-435">recordOrig</span></span>  
<span data-ttu-id="ad04b-436">すべての変更されたフィールドのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ad04b-436">A container of all changed fields.</span></span>

<!-- -->

<span data-ttu-id="ad04b-437">recordUpdated</span><span class="sxs-lookup"><span data-stu-id="ad04b-437">recordUpdated</span></span>  
<span data-ttu-id="ad04b-438">すべての変更されたフィールドのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ad04b-438">A container of all changed fields.</span></span>

<!-- -->

<span data-ttu-id="ad04b-439">changedFields</span><span class="sxs-lookup"><span data-stu-id="ad04b-439">changedFields</span></span>  
<span data-ttu-id="ad04b-440">すべての変更されたフィールドのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ad04b-440">A container of all changed fields.</span></span>

### <a name="remarks---eventupdate"></a><span data-ttu-id="ad04b-441">備考 - eventUpdate</span><span class="sxs-lookup"><span data-stu-id="ad04b-441">Remarks - eventUpdate</span></span>

<span data-ttu-id="ad04b-442">開発者は、特定のテーブルの更新時にコール バックするカーネルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-442">A developer can set up the kernel to call back on updates for a given table.</span></span> <span data-ttu-id="ad04b-443">これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventUpdate に設定することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-443">This is accomplished by inserting a record into the DatabaseLog kernel table with all fields set to relevant values, which includes setting the field logType to EventUpdate.</span></span> <span data-ttu-id="ad04b-444">レコードが更新されるとき、または特定のフィールドが更新されたときに必ず呼び出すカーネルを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-444">It is possible to set up the kernel to call back whenever a record is updated or when a specific field is updated.</span></span> <span data-ttu-id="ad04b-445">これは、logUpdate メソッドが呼び出されて設定される方法と非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="ad04b-445">This is very similar to how the logUpdate method is called and set up.</span></span> <span data-ttu-id="ad04b-446">このメソッドの呼び出しは、レコードが更新されたトランザクション内にあります。</span><span class="sxs-lookup"><span data-stu-id="ad04b-446">The call of this method will be in the transaction in which the record is updated.</span></span>

## <a name="method-transactionscopebegin"></a><span data-ttu-id="ad04b-447">メソッド transactionScopeBegin</span><span class="sxs-lookup"><span data-stu-id="ad04b-447">Method transactionScopeBegin</span></span>

```xpp
public void transactionScopeBegin()
```

## <a name="method-checkfornewbatchjobs"></a><span data-ttu-id="ad04b-448">メソッド checkForNewBatchJobs</span><span class="sxs-lookup"><span data-stu-id="ad04b-448">Method checkForNewBatchJobs</span></span>

```xpp
public static void checkForNewBatchJobs()
```

## <a name="method-disablecountrycontextfilter"></a><span data-ttu-id="ad04b-449">メソッド disableCountryContextFilter</span><span class="sxs-lookup"><span data-stu-id="ad04b-449">Method disableCountryContextFilter</span></span>

<span data-ttu-id="ad04b-450">現在の会社の国/地域のコンテキストに属さないフィールドが SELECT クエリから削除されるように、データ アクセス レイヤーでシステム全体の最適化を無効にします。</span><span class="sxs-lookup"><span data-stu-id="ad04b-450">Disables system-wide optimization in the data access layer, whereby fields that don't belong in the current company's country/region context are dropped from the SELECT query.</span></span>

```xpp
public void disableCountryContextFilter()
```

## <a name="method-xref"></a><span data-ttu-id="ad04b-451">メソッド xref</span><span class="sxs-lookup"><span data-stu-id="ad04b-451">Method xref</span></span>

```xpp
public void xref(str path, xRef x)
```

### <a name="parameters---xref"></a><span data-ttu-id="ad04b-452">パラメーター - xref</span><span class="sxs-lookup"><span data-stu-id="ad04b-452">Parameters - xref</span></span>

<span data-ttu-id="ad04b-453">path</span><span class="sxs-lookup"><span data-stu-id="ad04b-453">path</span></span>  

<!-- -->

<span data-ttu-id="ad04b-454">x</span><span class="sxs-lookup"><span data-stu-id="ad04b-454">x</span></span>  

## <a name="method-transactionscopeabort"></a><span data-ttu-id="ad04b-455">メソッド transactionScopeAbort</span><span class="sxs-lookup"><span data-stu-id="ad04b-455">Method transactionScopeAbort</span></span>

```xpp
public void transactionScopeAbort()
```

## <a name="method-eventrenamekey"></a><span data-ttu-id="ad04b-456">メソッド eventRenameKey</span><span class="sxs-lookup"><span data-stu-id="ad04b-456">Method eventRenameKey</span></span>

<span data-ttu-id="ad04b-457">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、主キーの名前が変更されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-457">Serves as a callback that is called by the kernel when a primary key is renamed, provided that the kernel has been set up to monitor records in that table.</span></span>

```xpp
public void eventRenameKey(Common recordOrig, Common recordUpdated, container changedFields)
```

### <a name="parameters---eventrenamekey"></a><span data-ttu-id="ad04b-458">パラメーター - eventRenameKey</span><span class="sxs-lookup"><span data-stu-id="ad04b-458">Parameters - eventRenameKey</span></span>

<span data-ttu-id="ad04b-459">recordOrig</span><span class="sxs-lookup"><span data-stu-id="ad04b-459">recordOrig</span></span>  
<span data-ttu-id="ad04b-460">すべての変更されたフィールドのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ad04b-460">A container of all changed fields.</span></span>

<!-- -->

<span data-ttu-id="ad04b-461">recordUpdated</span><span class="sxs-lookup"><span data-stu-id="ad04b-461">recordUpdated</span></span>  
<span data-ttu-id="ad04b-462">すべての変更されたフィールドのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ad04b-462">A container of all changed fields.</span></span>

<!-- -->

<span data-ttu-id="ad04b-463">changedFields</span><span class="sxs-lookup"><span data-stu-id="ad04b-463">changedFields</span></span>  
<span data-ttu-id="ad04b-464">すべての変更されたフィールドのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ad04b-464">A container of all changed fields.</span></span>

### <a name="remarks---eventrenamekey"></a><span data-ttu-id="ad04b-465">備考 - eventRenameKey</span><span class="sxs-lookup"><span data-stu-id="ad04b-465">Remarks - eventRenameKey</span></span>

<span data-ttu-id="ad04b-466">開発者は、特定のテーブルの主キーの名前の変更時にコール バックするカーネルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-466">A developer can set up the kernel to call back on primary key renames for a given table.</span></span> <span data-ttu-id="ad04b-467">これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventRenameKey に設定することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-467">This is accomplished by inserting a record into the DatabaseLog kernel table with all fields set to relevant values, which includes setting the field logType to EventRenameKey.</span></span> <span data-ttu-id="ad04b-468">これは、logRenameKey メソッドが呼び出されて設定される方法と非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="ad04b-468">This is very similar to how the logRenameKey method is called and set up.</span></span> <span data-ttu-id="ad04b-469">このメソッドの呼び出しは、主キーの名前が変更されたトランザクションになります。</span><span class="sxs-lookup"><span data-stu-id="ad04b-469">The call of this method will be in the transaction in which the primary key is renamed.</span></span>

## <a name="method-flushclientperformanceoptions"></a><span data-ttu-id="ad04b-470">メソッド flushClientPerformanceOptions</span><span class="sxs-lookup"><span data-stu-id="ad04b-470">Method flushClientPerformanceOptions</span></span>

```xpp
public void flushClientPerformanceOptions()
```

## <a name="method-flushclientservices"></a><span data-ttu-id="ad04b-471">メソッド flushClientServices</span><span class="sxs-lookup"><span data-stu-id="ad04b-471">Method flushClientServices</span></span>

```xpp
public static void flushClientServices()
```

## <a name="method-restartservicehost"></a><span data-ttu-id="ad04b-472">メソッド restartServiceHost</span><span class="sxs-lookup"><span data-stu-id="ad04b-472">Method restartServiceHost</span></span>

```xpp
public void restartServiceHost()
```

## <a name="method-updatexreftreenode"></a><span data-ttu-id="ad04b-473">メソッド updateXrefTreeNode</span><span class="sxs-lookup"><span data-stu-id="ad04b-473">Method updateXrefTreeNode</span></span>

<span data-ttu-id="ad04b-474">さまざまなノード タイプの相互参照情報が更新されると、フレームワークによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-474">Is invoked by the framework when cross-reference information for the various node types is updated.</span></span>

```xpp
public void updateXrefTreeNode(TreeNode treeNode)
```

### <a name="parameters---updatexreftreenode"></a><span data-ttu-id="ad04b-475">パラメーター - updateXrefTreeNode</span><span class="sxs-lookup"><span data-stu-id="ad04b-475">Parameters - updateXrefTreeNode</span></span>

<span data-ttu-id="ad04b-476">treeNode</span><span class="sxs-lookup"><span data-stu-id="ad04b-476">treeNode</span></span>  

### <a name="remarks---updatexreftreenode"></a><span data-ttu-id="ad04b-477">備考 - updateXrefTreeNode</span><span class="sxs-lookup"><span data-stu-id="ad04b-477">Remarks - updateXrefTreeNode</span></span>

<span data-ttu-id="ad04b-478">Application クラスは、過負荷機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-478">The Application class provides the overloaded functionality.</span></span>

## <a name="method-ttscommit"></a><span data-ttu-id="ad04b-479">メソッド ttscommit</span><span class="sxs-lookup"><span data-stu-id="ad04b-479">Method ttscommit</span></span>

```xpp
public void ttscommit()
```

## <a name="method-requestcompanychange"></a><span data-ttu-id="ad04b-480">メソッド RequestCompanyChange</span><span class="sxs-lookup"><span data-stu-id="ad04b-480">Method RequestCompanyChange</span></span>

```xpp
public void RequestCompanyChange([DataAreaSysCompany company])
```

### <a name="parameters---requestcompanychange"></a><span data-ttu-id="ad04b-481">パラメーター - RequestCompanyChange</span><span class="sxs-lookup"><span data-stu-id="ad04b-481">Parameters - RequestCompanyChange</span></span>

<span data-ttu-id="ad04b-482">会社</span><span class="sxs-lookup"><span data-stu-id="ad04b-482">company</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="ad04b-483">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="ad04b-483">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-eventinsert"></a><span data-ttu-id="ad04b-484">メソッド eventInsert</span><span class="sxs-lookup"><span data-stu-id="ad04b-484">Method eventInsert</span></span>

<span data-ttu-id="ad04b-485">そのテーブル内のレコードを監視するようにカーネルが設定されていれば、テーブル内のレコードが挿入されたときにカーネルにより呼び出されるコールバックとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ad04b-485">Serves as a callback that is called by the kernel when a record in a table is inserted, provided that the kernel has been set up to monitor records in that table.</span></span>

```xpp
public void eventInsert(Common recordInserted)
```

### <a name="parameters---eventinsert"></a><span data-ttu-id="ad04b-486">パラメーター - eventInsert</span><span class="sxs-lookup"><span data-stu-id="ad04b-486">Parameters - eventInsert</span></span>

<span data-ttu-id="ad04b-487">recordInserted</span><span class="sxs-lookup"><span data-stu-id="ad04b-487">recordInserted</span></span>  
<span data-ttu-id="ad04b-488">挿入済みレコード。</span><span class="sxs-lookup"><span data-stu-id="ad04b-488">The inserted record.</span></span>

### <a name="remarks---eventinsert"></a><span data-ttu-id="ad04b-489">備考 - eventInsert</span><span class="sxs-lookup"><span data-stu-id="ad04b-489">Remarks - eventInsert</span></span>

<span data-ttu-id="ad04b-490">開発者は、特定のテーブルの挿入時にコール バックするカーネルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-490">A developer can set up the kernel to call back on inserts for a given table.</span></span> <span data-ttu-id="ad04b-491">これは、関連する値に設定されたすべてのフィールドを持つ DatabaseLog カーネル テーブルにレコードを挿入することによって実行されます。これには、logType フィールドを EventInsert に設定することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ad04b-491">This is accomplished by inserting a record into the DatabaseLog kernel table with all fields set to relevant values, which includes setting the field logType to EventInsert.</span></span> <span data-ttu-id="ad04b-492">これは、logInsert メソッドが呼び出されて設定される方法と非常によく似ています。</span><span class="sxs-lookup"><span data-stu-id="ad04b-492">This is very similar to how logInsert method is called and set up.</span></span> <span data-ttu-id="ad04b-493">このメソッドの呼び出しは、レコードが挿入されたトランザクション内にあります。</span><span class="sxs-lookup"><span data-stu-id="ad04b-493">The call of this method will be in the transaction in which the record is inserted.</span></span>

## <a name="method-ttsnotifybegin"></a><span data-ttu-id="ad04b-494">メソッド ttsNotifyBegin</span><span class="sxs-lookup"><span data-stu-id="ad04b-494">Method ttsNotifyBegin</span></span>

```xpp
public void ttsNotifyBegin()
```

## <a name="method-closeallforms"></a><span data-ttu-id="ad04b-495">メソッド closeAllForms</span><span class="sxs-lookup"><span data-stu-id="ad04b-495">Method closeAllForms</span></span>

```xpp
public void closeAllForms()
```

## <a name="method-ttsnotifycommit"></a><span data-ttu-id="ad04b-496">メソッド ttsNotifyCommit</span><span class="sxs-lookup"><span data-stu-id="ad04b-496">Method ttsNotifyCommit</span></span>

```xpp
public void ttsNotifyCommit()
```

## <a name="method-ttsnotifyprecommit"></a><span data-ttu-id="ad04b-497">メソッド ttsNotifyPreCommit</span><span class="sxs-lookup"><span data-stu-id="ad04b-497">Method ttsNotifyPreCommit</span></span>

```xpp
public void ttsNotifyPreCommit()
```

## <a name="method-ttsnotifypostbegin"></a><span data-ttu-id="ad04b-498">メソッド ttsNotifyPostBegin</span><span class="sxs-lookup"><span data-stu-id="ad04b-498">Method ttsNotifyPostBegin</span></span>

```xpp
public void ttsNotifyPostBegin()
```

## <a name="method-ttsnotifyabort"></a><span data-ttu-id="ad04b-499">メソッド ttsNotifyAbort</span><span class="sxs-lookup"><span data-stu-id="ad04b-499">Method ttsNotifyAbort</span></span>

```xpp
public void ttsNotifyAbort()
```

## <a name="method-setdensity"></a><span data-ttu-id="ad04b-500">メソッド setDensity</span><span class="sxs-lookup"><span data-stu-id="ad04b-500">Method setDensity</span></span>

```xpp
public void setDensity([SysUserInfoDensity theme])
```

### <a name="parameters---setdensity"></a><span data-ttu-id="ad04b-501">パラメーター - setDensity</span><span class="sxs-lookup"><span data-stu-id="ad04b-501">Parameters - setDensity</span></span>

<span data-ttu-id="ad04b-502">theme</span><span class="sxs-lookup"><span data-stu-id="ad04b-502">theme</span></span>  

## <a name="method-loginsert"></a><span data-ttu-id="ad04b-503">メソッド logInsert</span><span class="sxs-lookup"><span data-stu-id="ad04b-503">Method logInsert</span></span>

```xpp
public void logInsert(Common recordInserted)
```

### <a name="parameters---loginsert"></a><span data-ttu-id="ad04b-504">パラメーター - logInsert</span><span class="sxs-lookup"><span data-stu-id="ad04b-504">Parameters - logInsert</span></span>

<span data-ttu-id="ad04b-505">recordInserted</span><span class="sxs-lookup"><span data-stu-id="ad04b-505">recordInserted</span></span>  

