---
title: ディクショナリ クラス
description: このトピックでは、ディクショナリ クラスについて説明します。
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
ms.openlocfilehash: d3b343d1fdafd695b3fea2d3febfbb2a9e3df2d7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502673"
---
# <a name="class-dictionary"></a><span data-ttu-id="f53c3-103">クラス ディクショナリ</span><span class="sxs-lookup"><span data-stu-id="f53c3-103">Class Dictionary</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Dictionary extends Object
```

<span data-ttu-id="f53c3-104">ディクショナリ クラスは、テーブル、拡張データ型、クラス、およびアプリケーション オブジェクト ツリー (AOT) の他の品目に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-104">The Dictionary class provides information about tables, extended data types, classes, and other items in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="f53c3-105">備考</span><span class="sxs-lookup"><span data-stu-id="f53c3-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f53c3-106">例</span><span class="sxs-lookup"><span data-stu-id="f53c3-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f53c3-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="f53c3-107">Methods</span></span>

| <span data-ttu-id="f53c3-108">方法</span><span class="sxs-lookup"><span data-stu-id="f53c3-108">Method</span></span>                                                                                                                                       | <span data-ttu-id="f53c3-109">説明</span><span class="sxs-lookup"><span data-stu-id="f53c3-109">Description</span></span>                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f53c3-110">public int classCnt()</span><span class="sxs-lookup"><span data-stu-id="f53c3-110">public int classCnt()</span></span>                                                                                                                        | <span data-ttu-id="f53c3-111">クラスの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-111">Indicates the number of classes.</span></span>                                                        |
| <span data-ttu-id="f53c3-112">public ClassId classCnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="f53c3-112">public ClassId classCnt2Id(int cnt)</span></span>                                                                                                          | <span data-ttu-id="f53c3-113">指定されたクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-113">Provides the ID of a specified class.</span></span>                                                                            |
| <span data-ttu-id="f53c3-114">public str className(ClassId classId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-114">public str className(ClassId classId)</span></span>                                                                                                        | <span data-ttu-id="f53c3-115">指定されたクラスの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-115">Provides the name of a specified class.</span></span>                                                                          |
| <span data-ttu-id="f53c3-116">public ClassId className2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="f53c3-116">public ClassId className2Id(str name)</span></span>                                                                                                        | <span data-ttu-id="f53c3-117">クラスの名前に基づいて、指定されたクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-117">Provides the ID for a specified class, based on the class name.</span></span>                                                  |
| <span data-ttu-id="f53c3-118">public ClassId classNext(ClassId classId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-118">public ClassId classNext(ClassId classId)</span></span>                                                                                                    | <span data-ttu-id="f53c3-119">クラス ID に基づいて、指定されたクラスの後に続くクラスを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-119">Indicates the class that succeeds a specified class, based on the class IDs.</span></span>                                     |
| <span data-ttu-id="f53c3-120">public DictClass classObject(ClassId classId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-120">public DictClass classObject(ClassId classId)</span></span>                                                                                                | <span data-ttu-id="f53c3-121">DictClass オブジェクトを返すことで、指定されたクラスに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-121">Provides information about a specified class by returning a DictClass object.</span></span>                                    |
| <span data-ttu-id="f53c3-122">public int configurationKeyCnt()</span><span class="sxs-lookup"><span data-stu-id="f53c3-122">public int configurationKeyCnt()</span></span>                                                                                                             | <span data-ttu-id="f53c3-123">コンフィギュレーション キーの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-123">Indicates the number of configuration keys.</span></span>                                             |
| <span data-ttu-id="f53c3-124">public ConfigurationKeyId configurationKeyCnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="f53c3-124">public ConfigurationKeyId configurationKeyCnt2Id(int cnt)</span></span>                                                                                    | <span data-ttu-id="f53c3-125">指定された構成キーの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-125">Provides the ID of a specified configuration key.</span></span>                                                                |
| <span data-ttu-id="f53c3-126">public str configurationKeyName(ConfigurationKeyId configurationKey)</span><span class="sxs-lookup"><span data-stu-id="f53c3-126">public str configurationKeyName(ConfigurationKeyId configurationKey)</span></span>                                                                         | <span data-ttu-id="f53c3-127">指定された構成キーの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-127">Provides the name of a specified configuration key.</span></span>                                                              |
| <span data-ttu-id="f53c3-128">public ConfigurationKeyId configurationKeyName2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="f53c3-128">public ConfigurationKeyId configurationKeyName2Id(str name)</span></span>                                                                                  | <span data-ttu-id="f53c3-129">構成キー名に基づいて、指定された構成キーの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-129">Provides the ID for a specified configuration key, based on the configuration key name.</span></span>                          |
| <span data-ttu-id="f53c3-130">public ConfigurationKeyId configurationKeyNext(ConfigurationKeyId configurationKey)</span><span class="sxs-lookup"><span data-stu-id="f53c3-130">public ConfigurationKeyId configurationKeyNext(ConfigurationKeyId configurationKey)</span></span>                                                          | <span data-ttu-id="f53c3-131">コンフィギュレーション キー ID に基づいて、指定されたコンフィギュレーション キーの後に続くコンフィギュレーション キーを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-131">Indicates the configuration key that succeeds a specified configuration key, based on the configuration key IDs.</span></span> |
| <span data-ttu-id="f53c3-132">public DictConfigurationKey configurationKeyObject(ConfigurationKeyId configurationKey)</span><span class="sxs-lookup"><span data-stu-id="f53c3-132">public DictConfigurationKey configurationKeyObject(ConfigurationKeyId configurationKey)</span></span>                                                      | <span data-ttu-id="f53c3-133">DictConfigurationKey オブジェクトを返すことで、指定された構成キーに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-133">Provides information about a specified configuration key by returning a DictConfigurationKey object.</span></span>             |
| <span data-ttu-id="f53c3-134">public SelectableDataArea currentCompany()</span><span class="sxs-lookup"><span data-stu-id="f53c3-134">public SelectableDataArea currentCompany()</span></span>                                                                                                   | <span data-ttu-id="f53c3-135">データベースでデータを使用できる現在の会社を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-135">Indicates the current company for which data is available in the database.</span></span>                                       |
| <span data-ttu-id="f53c3-136">public int enumCnt()</span><span class="sxs-lookup"><span data-stu-id="f53c3-136">public int enumCnt()</span></span>                                                                                                                         | <span data-ttu-id="f53c3-137">列挙型の数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-137">Indicates the number of enumeration types.</span></span>                                              |
| <span data-ttu-id="f53c3-138">public EnumId enumCnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="f53c3-138">public EnumId enumCnt2Id(int cnt)</span></span>                                                                                                            | <span data-ttu-id="f53c3-139">指定された列挙型タイプの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-139">Provides the ID of a specified enumeration type.</span></span>                                                                 |
| <span data-ttu-id="f53c3-140">public str enumName(EnumId typeId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-140">public str enumName(EnumId typeId)</span></span>                                                                                                           | <span data-ttu-id="f53c3-141">指定された列挙型の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-141">Provides the name for a specified enumeration.</span></span>                                                                   |
| <span data-ttu-id="f53c3-142">public EnumId enumName2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="f53c3-142">public EnumId enumName2Id(str name)</span></span>                                                                                                          | <span data-ttu-id="f53c3-143">名前に基づく、指定された列挙型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-143">Provides the ID of a specified enumeration, based on the name.</span></span>                                                   |
| <span data-ttu-id="f53c3-144">public EnumId enumNext(EnumId typeId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-144">public EnumId enumNext(EnumId typeId)</span></span>                                                                                                        | <span data-ttu-id="f53c3-145">列挙型 ID に基づいて、指定した列挙型の後に続く列挙型を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-145">Indicates the enumeration type that succeeds a specified enumeration type, based on the enumeration type IDs.</span></span>    |
| <span data-ttu-id="f53c3-146">public DictEnum enumObject(EnumId typeId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-146">public DictEnum enumObject(EnumId typeId)</span></span>                                                                                                    | <span data-ttu-id="f53c3-147">DictEnum オブジェクトを返すことで、指定された列挙型に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-147">Provides information about a specified enumeration by returning a DictEnum object.</span></span>                               |
| <span data-ttu-id="f53c3-148">public int licenseCodeCnt()</span><span class="sxs-lookup"><span data-stu-id="f53c3-148">public int licenseCodeCnt()</span></span>                                                                                                                  | <span data-ttu-id="f53c3-149">ライセンス コードの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-149">Indicates the number of license codes.</span></span>                                                  |
| <span data-ttu-id="f53c3-150">public LicenseCodeId licenseCodeCnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="f53c3-150">public LicenseCodeId licenseCodeCnt2Id(int cnt)</span></span>                                                                                              | <span data-ttu-id="f53c3-151">指定されたライセンス コードの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-151">Provides the ID of a specified license code.</span></span>                                                                     |
| <span data-ttu-id="f53c3-152">public str licenseCodeName(LicenseCodeId licenseCode)</span><span class="sxs-lookup"><span data-stu-id="f53c3-152">public str licenseCodeName(LicenseCodeId licenseCode)</span></span>                                                                                        | <span data-ttu-id="f53c3-153">指定されたライセンス コードの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-153">Provides the name of a specified license code.</span></span>                                                                   |
| <span data-ttu-id="f53c3-154">public LicenseCodeId licenseCodeName2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="f53c3-154">public LicenseCodeId licenseCodeName2Id(str name)</span></span>                                                                                            | <span data-ttu-id="f53c3-155">ライセンス コード名に基づいて、指定されたライセンス コードの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-155">Provides the ID for a specified license code, based on the license code name.</span></span>                                    |
| <span data-ttu-id="f53c3-156">public LicenseCodeId licenseCodeNext(LicenseCodeId licenseCode)</span><span class="sxs-lookup"><span data-stu-id="f53c3-156">public LicenseCodeId licenseCodeNext(LicenseCodeId licenseCode)</span></span>                                                                              | <span data-ttu-id="f53c3-157">ライセンス コード ID に基づいて、指定したライセンス コードの後に続くライセンス コードを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-157">Indicates the license code that succeeds a specified license code, based on the license code IDs.</span></span>                |
| <span data-ttu-id="f53c3-158">public DictLicenseCode licenseCodeObject(LicenseCodeId licenseCode)</span><span class="sxs-lookup"><span data-stu-id="f53c3-158">public DictLicenseCode licenseCodeObject(LicenseCodeId licenseCode)</span></span>                                                                          | <span data-ttu-id="f53c3-159">DictLicenseCode オブジェクトを返すことで、指定されたライセンス コードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-159">Provides information about a specified license code by returning a DictLicenseCode object.</span></span>                       |
| <span data-ttu-id="f53c3-160">public int tableCnt()</span><span class="sxs-lookup"><span data-stu-id="f53c3-160">public int tableCnt()</span></span>                                                                                                                        | <span data-ttu-id="f53c3-161">テーブルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-161">Indicates the number of tables.</span></span>                                                         |
| <span data-ttu-id="f53c3-162">public TableId tableCnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="f53c3-162">public TableId tableCnt2Id(int cnt)</span></span>                                                                                                          | <span data-ttu-id="f53c3-163">指定されたテーブルの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-163">Provides the ID of a specified table.</span></span>                                                                            |
| <span data-ttu-id="f53c3-164">public str tableName(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-164">public str tableName(TableId tableId)</span></span>                                                                                                        | <span data-ttu-id="f53c3-165">指定されたテーブルの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-165">Provides the name of a specified table.</span></span>                                                                          |
| <span data-ttu-id="f53c3-166">public TableId tableName2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="f53c3-166">public TableId tableName2Id(str name)</span></span>                                                                                                        | <span data-ttu-id="f53c3-167">テーブルの名前に基づいて、指定されたテーブルの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-167">Provides the ID for a specified table, based on the table name.</span></span>                                                  |
| <span data-ttu-id="f53c3-168">public TableId tableNext(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-168">public TableId tableNext(TableId tableId)</span></span>                                                                                                    | <span data-ttu-id="f53c3-169">テーブル ID に基づいて、指定されたテーブルの後に続くテーブルを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-169">Indicates the table that succeeds a specified table, based on the table IDs.</span></span>                                     |
| <span data-ttu-id="f53c3-170">public DictTable tableObject(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-170">public DictTable tableObject(TableId tableId)</span></span>                                                                                                | <span data-ttu-id="f53c3-171">DictTable オブジェクトを返すことで、指定されたテーブルに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-171">Provides information about a specified table by returning a DictTable object.</span></span>                                    |
| <span data-ttu-id="f53c3-172">public boolean tableSql(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-172">public boolean tableSql(TableId tableId)</span></span>                                                                                                     | <span data-ttu-id="f53c3-173">テーブルが SQL テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-173">Indicates whether a table is a SQL table.</span></span>                                                                        |
| <span data-ttu-id="f53c3-174">public boolean tableSystem(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-174">public boolean tableSystem(TableId tableId)</span></span>                                                                                                  | <span data-ttu-id="f53c3-175">テーブルがシステム テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-175">Indicates whether a table is a system table.</span></span>                                                                     |
| <span data-ttu-id="f53c3-176">public int testCode(int id, str value, str name, str serialno, str expiryDate, \[int userCount\], \[boolean verifyCert\], \[str timestamp\])</span><span class="sxs-lookup"><span data-stu-id="f53c3-176">public int testCode(int id, str value, str name, str serialno, str expiryDate, \[int userCount\], \[boolean verifyCert\], \[str timestamp\])</span></span> |                                                                                                                  |
| <span data-ttu-id="f53c3-177">public int typeCnt()</span><span class="sxs-lookup"><span data-stu-id="f53c3-177">public int typeCnt()</span></span>                                                                                                                         | <span data-ttu-id="f53c3-178">拡張データ型の数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-178">Indicates the number of extended data types.</span></span>                                            |
| <span data-ttu-id="f53c3-179">public ExtendedTypeId typeCnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="f53c3-179">public ExtendedTypeId typeCnt2Id(int cnt)</span></span>                                                                                                    | <span data-ttu-id="f53c3-180">指定された拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-180">Provides the ID of a specified extended data type.</span></span>                                                               |
| <span data-ttu-id="f53c3-181">public str typeName(ExtendedTypeId typeId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-181">public str typeName(ExtendedTypeId typeId)</span></span>                                                                                                   | <span data-ttu-id="f53c3-182">指定された拡張データ型の名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-182">Provides the name of a specified extended data type.</span></span>                                                             |
| <span data-ttu-id="f53c3-183">public ExtendedTypeId typeName2Id(str name)</span><span class="sxs-lookup"><span data-stu-id="f53c3-183">public ExtendedTypeId typeName2Id(str name)</span></span>                                                                                                  | <span data-ttu-id="f53c3-184">拡張データ型名に基づいて、指定された拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-184">Provides the ID for a specified extended data type, based on the extended data type name.</span></span>                        |
| <span data-ttu-id="f53c3-185">public ExtendedTypeId typeNext(ExtendedTypeId typeId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-185">public ExtendedTypeId typeNext(ExtendedTypeId typeId)</span></span>                                                                                        | <span data-ttu-id="f53c3-186">ID に基づいて、指定された拡張データ型の後に続く拡張データ型を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-186">Indicates the extended data type that succeeds a specified extended data type, based on the IDs.</span></span>                 |
| <span data-ttu-id="f53c3-187">public DictType typeObject(ExtendedTypeId typeId)</span><span class="sxs-lookup"><span data-stu-id="f53c3-187">public DictType typeObject(ExtendedTypeId typeId)</span></span>                                                                                            | <span data-ttu-id="f53c3-188">DictType オブジェクトを返すことで、指定された拡張データ型に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-188">Provides information about a specified extended data type by returning a DictType object.</span></span>                        |
| <span data-ttu-id="f53c3-189">::public static boolean safeMode()</span><span class="sxs-lookup"><span data-stu-id="f53c3-189">::public static boolean safeMode()</span></span>                                                                                                           |                                                                                                                  |
| <span data-ttu-id="f53c3-190">::public static void loginSettingsFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-190">::public static void loginSettingsFlush()</span></span>                                                                                                    | <span data-ttu-id="f53c3-191">ログオン設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-191">Refreshes the logon settings.</span></span>                                                          |
| <span data-ttu-id="f53c3-192">::public static void dataFlush(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="f53c3-192">::public static void dataFlush(\[TableId tableId\])</span></span>                                                                                          | <span data-ttu-id="f53c3-193">テーブル データを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-193">Refreshes the table data.</span></span>                                                               |
| <span data-ttu-id="f53c3-194">public void tableFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-194">public void tableFlush()</span></span>                                                                                                                     | <span data-ttu-id="f53c3-195">テーブを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-195">Refreshes the tables.</span></span>                                                                   |
| <span data-ttu-id="f53c3-196">public void enumFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-196">public void enumFlush()</span></span>                                                                                                                      | <span data-ttu-id="f53c3-197">列挙型を更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-197">Refreshes the enumeration types.</span></span>                                                        |
| <span data-ttu-id="f53c3-198">public void new()</span><span class="sxs-lookup"><span data-stu-id="f53c3-198">public void new()</span></span>                                                                                                                            | <span data-ttu-id="f53c3-199">Dictionary クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-199">Initializes a new instance of the Dictionary class.</span></span>                                                              |
| <span data-ttu-id="f53c3-200">public void classFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-200">public void classFlush()</span></span>                                                                                                                     | <span data-ttu-id="f53c3-201">クラスを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-201">Refreshes the classes.</span></span>                                                                  |
| <span data-ttu-id="f53c3-202">public void reloadSecurity(\[boolean reloadCodes\], \[boolean setSynchronizeRequired\], \[boolean flushTable\])</span><span class="sxs-lookup"><span data-stu-id="f53c3-202">public void reloadSecurity(\[boolean reloadCodes\], \[boolean setSynchronizeRequired\], \[boolean flushTable\])</span></span>                              | <span data-ttu-id="f53c3-203">機能キー システムを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="f53c3-203">Reloads the feature key system.</span></span>                                                                                  |
| <span data-ttu-id="f53c3-204">public void typeFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-204">public void typeFlush()</span></span>                                                                                                                      | <span data-ttu-id="f53c3-205">拡張データ型を更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-205">Refreshes the extended data types.</span></span>                                                      |
| <span data-ttu-id="f53c3-206">public void configurationKeyFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-206">public void configurationKeyFlush()</span></span>                                                                                                          | <span data-ttu-id="f53c3-207">コンフィギュレーション キーを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-207">Refreshes the configuration keys.</span></span>                                                       |
| <span data-ttu-id="f53c3-208">public void licenseCodeFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-208">public void licenseCodeFlush()</span></span>                                                                                                               | <span data-ttu-id="f53c3-209">ライセンス コードを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-209">Refreshes the license codes.</span></span>                                                            |
| <span data-ttu-id="f53c3-210">::public static void aodFlush()</span><span class="sxs-lookup"><span data-stu-id="f53c3-210">::public static void aodFlush()</span></span>                                                                                                              | <span data-ttu-id="f53c3-211">.aod ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-211">Refreshes the .aod file.</span></span>                                                                                         |

## <a name="method-classcnt"></a><span data-ttu-id="f53c3-212">メソッド classCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-212">Method classCnt</span></span>

<span data-ttu-id="f53c3-213">クラスの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-213">Indicates the number of classes.</span></span>

```xpp
public int classCnt()
```

### <a name="return-value---classcnt"></a><span data-ttu-id="f53c3-214">戻り値 - classCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-214">Return Value - classCnt</span></span>

<span data-ttu-id="f53c3-215">クラスの数を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-215">An integer value that indicates the number of classes.</span></span>

## <a name="method-classcnt2id"></a><span data-ttu-id="f53c3-216">メソッド classCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-216">Method classCnt2Id</span></span>

<span data-ttu-id="f53c3-217">指定されたクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-217">Provides the ID of a specified class.</span></span>

```xpp
public ClassId classCnt2Id(int cnt)
```

### <a name="parameters---classcnt2id"></a><span data-ttu-id="f53c3-218">パラメーター - classCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-218">Parameters - classCnt2Id</span></span>

<span data-ttu-id="f53c3-219">cnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-219">cnt</span></span>  
<span data-ttu-id="f53c3-220">クラスの順序に基づいてクラスを指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-220">An integer value that specifies a class, based on the order of classes.</span></span>

### <a name="return-value---classcnt2id"></a><span data-ttu-id="f53c3-221">戻り値 - classCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-221">Return Value - classCnt2Id</span></span>

<span data-ttu-id="f53c3-222">クラス ID を示す classId システム データ型値。Dictionary::classCnt メソッドによって返されるクラスの数より大きな cnt 値を渡すと 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f53c3-222">A classId system data type value that indicates the class ID; 0 (zero) if you pass a cnt value that is larger than the number of classes that is returned by the Dictionary::classCnt method.</span></span>

## <a name="method-classname"></a><span data-ttu-id="f53c3-223">メソッド className</span><span class="sxs-lookup"><span data-stu-id="f53c3-223">Method className</span></span>

<span data-ttu-id="f53c3-224">指定されたクラスの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-224">Provides the name of a specified class.</span></span>

```xpp
public str className(ClassId classId)
```

### <a name="parameters---classname"></a><span data-ttu-id="f53c3-225">パラメーター - className</span><span class="sxs-lookup"><span data-stu-id="f53c3-225">Parameters - className</span></span>

<span data-ttu-id="f53c3-226">classId</span><span class="sxs-lookup"><span data-stu-id="f53c3-226">classId</span></span>  
<span data-ttu-id="f53c3-227">クラス ID を示す classId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-227">A classId system data type that indicates the class ID.</span></span>

### <a name="return-value---classname"></a><span data-ttu-id="f53c3-228">戻り値 - className</span><span class="sxs-lookup"><span data-stu-id="f53c3-228">Return Value - className</span></span>

<span data-ttu-id="f53c3-229">クラス名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-229">A string that indicates the class name.</span></span>

### <a name="remarks---classname"></a><span data-ttu-id="f53c3-230">備考 - className</span><span class="sxs-lookup"><span data-stu-id="f53c3-230">Remarks - className</span></span>

<span data-ttu-id="f53c3-231">クラス ID は、符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-231">Class IDs are unsigned integers.</span></span>

## <a name="method-classname2id"></a><span data-ttu-id="f53c3-232">メソッド className2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-232">Method className2Id</span></span>

<span data-ttu-id="f53c3-233">クラスの名前に基づいて、指定されたクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-233">Provides the ID for a specified class, based on the class name.</span></span>

```xpp
public ClassId className2Id(str name)
```

### <a name="parameters---classname2id"></a><span data-ttu-id="f53c3-234">パラメーター - className2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-234">Parameters - className2Id</span></span>

<span data-ttu-id="f53c3-235">名前</span><span class="sxs-lookup"><span data-stu-id="f53c3-235">name</span></span>  
<span data-ttu-id="f53c3-236">クラス名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-236">A string that indicates the class name.</span></span>

### <a name="return-value---classname2id"></a><span data-ttu-id="f53c3-237">戻り値 - className2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-237">Return Value - className2Id</span></span>

<span data-ttu-id="f53c3-238">クラス ID を示す classId システム データ型値; 存在しないクラスの名前値を渡すと 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f53c3-238">A classId system data type value that indicates the class ID; 0 (zero) if you pass a name value for a nonexistent class.</span></span>

## <a name="method-classnext"></a><span data-ttu-id="f53c3-239">メソッド classNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-239">Method classNext</span></span>

<span data-ttu-id="f53c3-240">クラス ID に基づいて、指定されたクラスの後に続くクラスを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-240">Indicates the class that succeeds a specified class, based on the class IDs.</span></span>

```xpp
public ClassId classNext(ClassId classId)
```

### <a name="parameters---classnext"></a><span data-ttu-id="f53c3-241">パラメーター - classNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-241">Parameters - classNext</span></span>

<span data-ttu-id="f53c3-242">classId</span><span class="sxs-lookup"><span data-stu-id="f53c3-242">classId</span></span>  
<span data-ttu-id="f53c3-243">クラス ID を示す classId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-243">A classId system data type that indicates a class ID.</span></span>

### <a name="return-value---classnext"></a><span data-ttu-id="f53c3-244">戻り値 - classNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-244">Return Value - classNext</span></span>

<span data-ttu-id="f53c3-245">指定されたクラスを継承するクラスを示す classId システム データ型値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-245">A classId system data type value that indicates the class that succeeds the specified class.</span></span>

## <a name="method-classobject"></a><span data-ttu-id="f53c3-246">メソッド classObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-246">Method classObject</span></span>

<span data-ttu-id="f53c3-247">DictClass オブジェクトを返すことで、指定されたクラスに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-247">Provides information about a specified class by returning a DictClass object.</span></span>

```xpp
public DictClass classObject(ClassId classId)
```

### <a name="parameters---classobject"></a><span data-ttu-id="f53c3-248">パラメーター - classObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-248">Parameters - classObject</span></span>

<span data-ttu-id="f53c3-249">classId</span><span class="sxs-lookup"><span data-stu-id="f53c3-249">classId</span></span>  
<span data-ttu-id="f53c3-250">クラス ID を示す classId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-250">A classId system data type that indicates a class ID.</span></span>

### <a name="return-value---classobject"></a><span data-ttu-id="f53c3-251">戻り値 - classObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-251">Return Value - classObject</span></span>

<span data-ttu-id="f53c3-252">指定されたクラスに関する情報を含む DictClass オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f53c3-252">A DictClass object that contains information about the specified class.</span></span>

## <a name="method-configurationkeycnt"></a><span data-ttu-id="f53c3-253">メソッド configurationKeyCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-253">Method configurationKeyCnt</span></span>

<span data-ttu-id="f53c3-254">コンフィギュレーション キーの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-254">Indicates the number of configuration keys.</span></span>

```xpp
public int configurationKeyCnt()
```

### <a name="return-value---configurationkeycnt"></a><span data-ttu-id="f53c3-255">戻り値 - configurationKeyCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-255">Return Value - configurationKeyCnt</span></span>

<span data-ttu-id="f53c3-256">コンフィギュレーション キーの数を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-256">An integer value that indicates the number of configuration keys.</span></span>

## <a name="method-configurationkeycnt2id"></a><span data-ttu-id="f53c3-257">メソッド configurationKeyCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-257">Method configurationKeyCnt2Id</span></span>

<span data-ttu-id="f53c3-258">指定された構成キーの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-258">Provides the ID of a specified configuration key.</span></span>

```xpp
public ConfigurationKeyId configurationKeyCnt2Id(int cnt)
```

### <a name="parameters---configurationkeycnt2id"></a><span data-ttu-id="f53c3-259">パラメーター - configurationKeyCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-259">Parameters - configurationKeyCnt2Id</span></span>

<span data-ttu-id="f53c3-260">cnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-260">cnt</span></span>  
<span data-ttu-id="f53c3-261">コンフィギュレーション キーの順序に基づいてコンフィギュレーション キーを指定する整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-261">An integer that specifies a configuration key, based on the order of configuration keys.</span></span>

### <a name="return-value---configurationkeycnt2id"></a><span data-ttu-id="f53c3-262">戻り値 - configurationKeyCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-262">Return Value - configurationKeyCnt2Id</span></span>

<span data-ttu-id="f53c3-263">コンフィギュレーション キー ID を示す configurationKeyId システム データ型値。Dictionary::configurationKeyCnt メソッドから返されるコンフィギュレーション キーの数よりも大きい cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="f53c3-263">A configurationKeyId system data type value that indicates a configuration key ID; 0 (zero) if you pass a cnt value that is larger than the number of configuration keys that is returned by the Dictionary::configurationKeyCnt method.</span></span>

## <a name="method-configurationkeyname"></a><span data-ttu-id="f53c3-264">メソッド configurationKeyName</span><span class="sxs-lookup"><span data-stu-id="f53c3-264">Method configurationKeyName</span></span>

<span data-ttu-id="f53c3-265">指定された構成キーの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-265">Provides the name of a specified configuration key.</span></span>

```xpp
public str configurationKeyName(ConfigurationKeyId configurationKey)
```

### <a name="parameters---configurationkeyname"></a><span data-ttu-id="f53c3-266">パラメーター - configurationKeyName</span><span class="sxs-lookup"><span data-stu-id="f53c3-266">Parameters - configurationKeyName</span></span>

<span data-ttu-id="f53c3-267">configurationKey</span><span class="sxs-lookup"><span data-stu-id="f53c3-267">configurationKey</span></span>  
<span data-ttu-id="f53c3-268">コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-268">A configurationKeyId system data type that indicates a configuration key ID.</span></span>

### <a name="return-value---configurationkeyname"></a><span data-ttu-id="f53c3-269">戻り値 - configurationKeyName</span><span class="sxs-lookup"><span data-stu-id="f53c3-269">Return Value - configurationKeyName</span></span>

<span data-ttu-id="f53c3-270">コンフィギュレーション キーの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-270">A string that indicates the name of the configuration key.</span></span>

## <a name="method-configurationkeyname2id"></a><span data-ttu-id="f53c3-271">メソッド configurationKeyName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-271">Method configurationKeyName2Id</span></span>

<span data-ttu-id="f53c3-272">構成キー名に基づいて、指定された構成キーの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-272">Provides the ID for a specified configuration key, based on the configuration key name.</span></span>

```xpp
public ConfigurationKeyId configurationKeyName2Id(str name)
```

### <a name="parameters---configurationkeyname2id"></a><span data-ttu-id="f53c3-273">パラメーター - configurationKeyName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-273">Parameters - configurationKeyName2Id</span></span>

<span data-ttu-id="f53c3-274">名前</span><span class="sxs-lookup"><span data-stu-id="f53c3-274">name</span></span>  
<span data-ttu-id="f53c3-275">コンフィギュレーション キーの名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-275">A string that indicates a configuration key name.</span></span>

### <a name="return-value---configurationkeyname2id"></a><span data-ttu-id="f53c3-276">戻り値 - configurationKeyName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-276">Return Value - configurationKeyName2Id</span></span>

<span data-ttu-id="f53c3-277">コンフィギュレーション キー ID を示す configurationKeyId システム データ型値; 存在しないコンフィギュレーション キー の名前の値を渡すと、0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="f53c3-277">A configurationKeyId system data type value that indicates the configuration key ID; 0 (zero) if you pass a name value for a nonexistent configuration key.</span></span>

## <a name="method-configurationkeynext"></a><span data-ttu-id="f53c3-278">メソッド configurationKeyNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-278">Method configurationKeyNext</span></span>

<span data-ttu-id="f53c3-279">コンフィギュレーション キー ID に基づいて、指定されたコンフィギュレーション キーの後に続くコンフィギュレーション キーを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-279">Indicates the configuration key that succeeds a specified configuration key, based on the configuration key IDs.</span></span>

```xpp
public ConfigurationKeyId configurationKeyNext(ConfigurationKeyId configurationKey)
```

### <a name="parameters---configurationkeynext"></a><span data-ttu-id="f53c3-280">パラメーター - configurationKeyNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-280">Parameters - configurationKeyNext</span></span>

<span data-ttu-id="f53c3-281">configurationKey</span><span class="sxs-lookup"><span data-stu-id="f53c3-281">configurationKey</span></span>  
<span data-ttu-id="f53c3-282">コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-282">A configurationKeyId system data type that indicates a configuration key ID.</span></span>

### <a name="return-value---configurationkeynext"></a><span data-ttu-id="f53c3-283">戻り値 - configurationKeyNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-283">Return Value - configurationKeyNext</span></span>

<span data-ttu-id="f53c3-284">指定されたコンフィギュレーション キー の後に続くコンフィギュレーション キーの configurationKeyId システム データ型値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-284">A configurationKeyId system data type value for the configuration key that succeeds the specified configuration key.</span></span>

## <a name="method-configurationkeyobject"></a><span data-ttu-id="f53c3-285">メソッド configurationKeyObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-285">Method configurationKeyObject</span></span>

<span data-ttu-id="f53c3-286">DictConfigurationKey オブジェクトを返すことで、指定された構成キーに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-286">Provides information about a specified configuration key by returning a DictConfigurationKey object.</span></span>

```xpp
public DictConfigurationKey configurationKeyObject(ConfigurationKeyId configurationKey)
```

### <a name="parameters---configurationkeyobject"></a><span data-ttu-id="f53c3-287">パラメーター - configurationKeyObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-287">Parameters - configurationKeyObject</span></span>

<span data-ttu-id="f53c3-288">configurationKey</span><span class="sxs-lookup"><span data-stu-id="f53c3-288">configurationKey</span></span>  
<span data-ttu-id="f53c3-289">コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-289">A configurationKeyId system data type that indicates a configuration key ID.</span></span>

### <a name="return-value---configurationkeyobject"></a><span data-ttu-id="f53c3-290">戻り値 - configurationKeyObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-290">Return Value - configurationKeyObject</span></span>

<span data-ttu-id="f53c3-291">指定されたコンフィギュレーション キーに関する情報を含む DictConfigurationKey オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f53c3-291">A DictConfigurationKey object that contains information about the specified configuration key.</span></span>

## <a name="method-currentcompany"></a><span data-ttu-id="f53c3-292">メソッド currentCompany</span><span class="sxs-lookup"><span data-stu-id="f53c3-292">Method currentCompany</span></span>

<span data-ttu-id="f53c3-293">データベースでデータを使用できる現在の会社を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-293">Indicates the current company for which data is available in the database.</span></span>

```xpp
public SelectableDataArea currentCompany()
```

### <a name="return-value---currentcompany"></a><span data-ttu-id="f53c3-294">戻り値 - currentCompany</span><span class="sxs-lookup"><span data-stu-id="f53c3-294">Return Value - currentCompany</span></span>

<span data-ttu-id="f53c3-295">現在の会社を示す SelectableDataArea システムのデータ型の値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-295">A selectableDataArea system data type value that indicates the current company.</span></span>

## <a name="method-enumcnt"></a><span data-ttu-id="f53c3-296">メソッド enumCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-296">Method enumCnt</span></span>

<span data-ttu-id="f53c3-297">列挙型の数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-297">Indicates the number of enumeration types.</span></span>

```xpp
public int enumCnt()
```

### <a name="return-value---enumcnt"></a><span data-ttu-id="f53c3-298">戻り値 - enumCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-298">Return Value - enumCnt</span></span>

<span data-ttu-id="f53c3-299">列挙型の数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-299">An integer that indicates the number of enumeration types.</span></span>

## <a name="method-enumcnt2id"></a><span data-ttu-id="f53c3-300">メソッド enumCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-300">Method enumCnt2Id</span></span>

<span data-ttu-id="f53c3-301">指定された列挙型タイプの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-301">Provides the ID of a specified enumeration type.</span></span>

```xpp
public EnumId enumCnt2Id(int cnt)
```

### <a name="parameters---enumcnt2id"></a><span data-ttu-id="f53c3-302">パラメーター - enumCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-302">Parameters - enumCnt2Id</span></span>

<span data-ttu-id="f53c3-303">cnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-303">cnt</span></span>  
<span data-ttu-id="f53c3-304">列挙型の順序に基づいて列挙型を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-304">An integer that specifies an enumeration type, based on the order of enumeration types.</span></span>

### <a name="return-value---enumcnt2id"></a><span data-ttu-id="f53c3-305">戻り値 - enumCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-305">Return Value - enumCnt2Id</span></span>

<span data-ttu-id="f53c3-306">列挙型 ID を示す enumId システム データ型値です。Dictionary::enumCnt メソッドによって返されるクラスの数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="f53c3-306">An enumId system data type value that indicates the enumeration type ID; 0 (zero) if you pass a cnt value that is larger than the number of classes that is returned by the Dictionary::enumCnt method.</span></span>

## <a name="method-enumname"></a><span data-ttu-id="f53c3-307">メソッド enumName</span><span class="sxs-lookup"><span data-stu-id="f53c3-307">Method enumName</span></span>

<span data-ttu-id="f53c3-308">指定された列挙型の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-308">Provides the name for a specified enumeration.</span></span>

```xpp
public str enumName(EnumId typeId)
```

### <a name="parameters---enumname"></a><span data-ttu-id="f53c3-309">パラメーター - enumName</span><span class="sxs-lookup"><span data-stu-id="f53c3-309">Parameters - enumName</span></span>

<span data-ttu-id="f53c3-310">typeId</span><span class="sxs-lookup"><span data-stu-id="f53c3-310">typeId</span></span>  
<span data-ttu-id="f53c3-311">列挙の enumId システム データ型です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-311">An enumId system data type for an enumeration.</span></span>

### <a name="return-value---enumname"></a><span data-ttu-id="f53c3-312">戻り値 - enumName</span><span class="sxs-lookup"><span data-stu-id="f53c3-312">Return Value - enumName</span></span>

<span data-ttu-id="f53c3-313">列挙の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-313">A string that indicates the name of the enumeration.</span></span>

## <a name="method-enumname2id"></a><span data-ttu-id="f53c3-314">メソッド enumName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-314">Method enumName2Id</span></span>

<span data-ttu-id="f53c3-315">名前に基づく、指定された列挙型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-315">Provides the ID of a specified enumeration, based on the name.</span></span>

```xpp
public EnumId enumName2Id(str name)
```

### <a name="parameters---enumname2id"></a><span data-ttu-id="f53c3-316">パラメーター - enumName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-316">Parameters - enumName2Id</span></span>

<span data-ttu-id="f53c3-317">名前</span><span class="sxs-lookup"><span data-stu-id="f53c3-317">name</span></span>  
<span data-ttu-id="f53c3-318">列挙の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-318">A string that indicates the name of an enumeration.</span></span>

### <a name="return-value---enumname2id"></a><span data-ttu-id="f53c3-319">戻り値 - enumName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-319">Return Value - enumName2Id</span></span>

<span data-ttu-id="f53c3-320">列挙の ID を示す enumId システム データ型値です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-320">An enumId system data type value that indicates the ID of the enumeration.</span></span>

## <a name="method-enumnext"></a><span data-ttu-id="f53c3-321">メソッド enumNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-321">Method enumNext</span></span>

<span data-ttu-id="f53c3-322">列挙型 ID に基づいて、指定した列挙型の後に続く列挙型を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-322">Indicates the enumeration type that succeeds a specified enumeration type, based on the enumeration type IDs.</span></span>

```xpp
public EnumId enumNext(EnumId typeId)
```

### <a name="parameters---enumnext"></a><span data-ttu-id="f53c3-323">パラメーター - enumNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-323">Parameters - enumNext</span></span>

<span data-ttu-id="f53c3-324">typeId</span><span class="sxs-lookup"><span data-stu-id="f53c3-324">typeId</span></span>  
<span data-ttu-id="f53c3-325">列挙 ID を示す enumId システム データ型です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-325">An enumId system data type that indicates an enumeration ID.</span></span>

### <a name="return-value---enumnext"></a><span data-ttu-id="f53c3-326">戻り値 - enumNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-326">Return Value - enumNext</span></span>

<span data-ttu-id="f53c3-327">指定された列挙を継承する列挙の enumId システム データ型値です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-327">An enumId system data type value for the enumeration that succeeds the specified enumeration.</span></span>

## <a name="method-enumobject"></a><span data-ttu-id="f53c3-328">メソッド enumObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-328">Method enumObject</span></span>

<span data-ttu-id="f53c3-329">DictEnum オブジェクトを返すことで、指定された列挙型に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-329">Provides information about a specified enumeration by returning a DictEnum object.</span></span>

```xpp
public DictEnum enumObject(EnumId typeId)
```

### <a name="parameters---enumobject"></a><span data-ttu-id="f53c3-330">パラメーター - enumObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-330">Parameters - enumObject</span></span>

<span data-ttu-id="f53c3-331">typeId</span><span class="sxs-lookup"><span data-stu-id="f53c3-331">typeId</span></span>  
<span data-ttu-id="f53c3-332">列挙 ID を示す enumId システム データ型です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-332">An enumId system data type that indicates an enumeration ID.</span></span>

### <a name="return-value---enumobject"></a><span data-ttu-id="f53c3-333">戻り値 - enumObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-333">Return Value - enumObject</span></span>

<span data-ttu-id="f53c3-334">指定された列挙に関する情報を含む DictEnum オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f53c3-334">A DictEnum object that contains information about the specified enumeration.</span></span>

## <a name="method-licensecodecnt"></a><span data-ttu-id="f53c3-335">メソッド licenseCodeCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-335">Method licenseCodeCnt</span></span>

<span data-ttu-id="f53c3-336">ライセンス コードの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-336">Indicates the number of license codes.</span></span>

```xpp
public int licenseCodeCnt()
```

### <a name="return-value---licensecodecnt"></a><span data-ttu-id="f53c3-337">戻り値 - licenseCodeCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-337">Return Value - licenseCodeCnt</span></span>

<span data-ttu-id="f53c3-338">ライセンス コードの数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-338">An integer that indicates the number of license codes.</span></span>

## <a name="method-licensecodecnt2id"></a><span data-ttu-id="f53c3-339">メソッド licenseCodeCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-339">Method licenseCodeCnt2Id</span></span>

<span data-ttu-id="f53c3-340">指定されたライセンス コードの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-340">Provides the ID of a specified license code.</span></span>

```xpp
public LicenseCodeId licenseCodeCnt2Id(int cnt)
```

### <a name="parameters---licensecodecnt2id"></a><span data-ttu-id="f53c3-341">パラメーター - licenseCodeCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-341">Parameters - licenseCodeCnt2Id</span></span>

<span data-ttu-id="f53c3-342">cnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-342">cnt</span></span>  
<span data-ttu-id="f53c3-343">ライセンス コードの順序に基づいてライセンス コードを指定する整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-343">An integer that specifies a license code, based on the order of license codes.</span></span>

### <a name="return-value---licensecodecnt2id"></a><span data-ttu-id="f53c3-344">戻り値 - licenseCodeCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-344">Return Value - licenseCodeCnt2Id</span></span>

<span data-ttu-id="f53c3-345">ライセンス コード ID を示す licenseCodeId システム データ型値。Dictionary::licenseCodeCnt メソッドによって返されるライセンス コードの数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="f53c3-345">A licenseCodeId system data type value that indicates the license code ID; 0 (zero) if you pass a cnt value that is larger than the number of license codes that is returned by the Dictionary::licenseCodeCnt method.</span></span>

## <a name="method-licensecodename"></a><span data-ttu-id="f53c3-346">メソッド licenseCodeName</span><span class="sxs-lookup"><span data-stu-id="f53c3-346">Method licenseCodeName</span></span>

<span data-ttu-id="f53c3-347">指定されたライセンス コードの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-347">Provides the name of a specified license code.</span></span>

```xpp
public str licenseCodeName(LicenseCodeId licenseCode)
```

### <a name="parameters---licensecodename"></a><span data-ttu-id="f53c3-348">パラメーター - licenseCodeName</span><span class="sxs-lookup"><span data-stu-id="f53c3-348">Parameters - licenseCodeName</span></span>

<span data-ttu-id="f53c3-349">licenseCode</span><span class="sxs-lookup"><span data-stu-id="f53c3-349">licenseCode</span></span>  
<span data-ttu-id="f53c3-350">ライセンス コード ID を示す licenseCodeId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-350">A licenseCodeId system data type that indicates the license code ID.</span></span>

### <a name="return-value---licensecodename"></a><span data-ttu-id="f53c3-351">戻り値 - licenseCodeName</span><span class="sxs-lookup"><span data-stu-id="f53c3-351">Return Value - licenseCodeName</span></span>

<span data-ttu-id="f53c3-352">ライセンス コード名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-352">A string that indicates the license code name.</span></span>

## <a name="method-licensecodename2id"></a><span data-ttu-id="f53c3-353">メソッド licenseCodeName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-353">Method licenseCodeName2Id</span></span>

<span data-ttu-id="f53c3-354">ライセンス コード名に基づいて、指定されたライセンス コードの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-354">Provides the ID for a specified license code, based on the license code name.</span></span>

```xpp
public LicenseCodeId licenseCodeName2Id(str name)
```

### <a name="parameters---licensecodename2id"></a><span data-ttu-id="f53c3-355">パラメーター - licenseCodeName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-355">Parameters - licenseCodeName2Id</span></span>

<span data-ttu-id="f53c3-356">名前</span><span class="sxs-lookup"><span data-stu-id="f53c3-356">name</span></span>  
<span data-ttu-id="f53c3-357">ライセンス コード名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-357">A string that indicates the license code name.</span></span>

### <a name="return-value---licensecodename2id"></a><span data-ttu-id="f53c3-358">戻り値 - licenseCodeName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-358">Return Value - licenseCodeName2Id</span></span>

<span data-ttu-id="f53c3-359">ライセンス コード ID を示す licenseCodeId システム データ型の値、存在しないライセンス コード名の値を渡すと 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f53c3-359">A licenseCodeId system data type value that indicates the license code ID; 0 (zero) if you pass a name value for a nonexistent license code.</span></span>

## <a name="method-licensecodenext"></a><span data-ttu-id="f53c3-360">メソッド licenseCodeNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-360">Method licenseCodeNext</span></span>

<span data-ttu-id="f53c3-361">ライセンス コード ID に基づいて、指定したライセンス コードの後に続くライセンス コードを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-361">Indicates the license code that succeeds a specified license code, based on the license code IDs.</span></span>

```xpp
public LicenseCodeId licenseCodeNext(LicenseCodeId licenseCode)
```

### <a name="parameters---licensecodenext"></a><span data-ttu-id="f53c3-362">パラメーター - licenseCodeNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-362">Parameters - licenseCodeNext</span></span>

<span data-ttu-id="f53c3-363">licenseCode</span><span class="sxs-lookup"><span data-stu-id="f53c3-363">licenseCode</span></span>  
<span data-ttu-id="f53c3-364">ライセンス コード ID を示す licenseCodeId システム データ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-364">A licenseCodeId system data type that indicates a license code ID.</span></span>

### <a name="return-value---licensecodenext"></a><span data-ttu-id="f53c3-365">戻り値 - licenseCodeNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-365">Return Value - licenseCodeNext</span></span>

<span data-ttu-id="f53c3-366">指定したライセンス コードの後に続くライセンス コードの licenseCodeId システム データ型の値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-366">A licenseCodeId system data type value for the license code that succeeds the specified license code.</span></span>

## <a name="method-licensecodeobject"></a><span data-ttu-id="f53c3-367">メソッド licenseCodeObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-367">Method licenseCodeObject</span></span>

<span data-ttu-id="f53c3-368">DictLicenseCode オブジェクトを返すことで、指定されたライセンス コードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-368">Provides information about a specified license code by returning a DictLicenseCode object.</span></span>

```xpp
public DictLicenseCode licenseCodeObject(LicenseCodeId licenseCode)
```

### <a name="parameters---licensecodeobject"></a><span data-ttu-id="f53c3-369">パラメーター - licenseCodeObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-369">Parameters - licenseCodeObject</span></span>

<span data-ttu-id="f53c3-370">licenseCode</span><span class="sxs-lookup"><span data-stu-id="f53c3-370">licenseCode</span></span>  
<span data-ttu-id="f53c3-371">ライセンス コード ID を示す licenseCodeId システム データ。</span><span class="sxs-lookup"><span data-stu-id="f53c3-371">A licenseCodeId system data that indicates a license code ID.</span></span>

### <a name="return-value---licensecodeobject"></a><span data-ttu-id="f53c3-372">戻り値 - licenseCodeObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-372">Return Value - licenseCodeObject</span></span>

<span data-ttu-id="f53c3-373">指定されたライセンス コードに関する情報を含む DictLicenseCode オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f53c3-373">A DictLicenseCode object that contains information about the specified license code.</span></span>

## <a name="method-tablecnt"></a><span data-ttu-id="f53c3-374">メソッド tableCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-374">Method tableCnt</span></span>

<span data-ttu-id="f53c3-375">テーブルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-375">Indicates the number of tables.</span></span>

```xpp
public int tableCnt()
```

### <a name="return-value---tablecnt"></a><span data-ttu-id="f53c3-376">戻り値 - tableCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-376">Return Value - tableCnt</span></span>

<span data-ttu-id="f53c3-377">テーブルの数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-377">An integer that indicates the number of tables.</span></span>

## <a name="method-tablecnt2id"></a><span data-ttu-id="f53c3-378">メソッド tableCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-378">Method tableCnt2Id</span></span>

<span data-ttu-id="f53c3-379">指定されたテーブルの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-379">Provides the ID of a specified table.</span></span>

```xpp
public TableId tableCnt2Id(int cnt)
```

### <a name="parameters---tablecnt2id"></a><span data-ttu-id="f53c3-380">パラメーター - tableCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-380">Parameters - tableCnt2Id</span></span>

<span data-ttu-id="f53c3-381">cnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-381">cnt</span></span>  
<span data-ttu-id="f53c3-382">テーブルの順序に基づく、テーブルを指定する整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-382">An integer that specifies a table, based on the order of tables.</span></span>

### <a name="return-value---tablecnt2id"></a><span data-ttu-id="f53c3-383">戻り値 - tableCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-383">Return Value - tableCnt2Id</span></span>

<span data-ttu-id="f53c3-384">テーブル ID を示す TableId システムのデータ型値。Dictionary::tableCnt メソッドによって返されるテーブル数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f53c3-384">A tableId system data type value that indicates the table ID; 0 (zero) if you pass a cnt value that is larger than the number of tables that is returned by the Dictionary::tableCnt method.</span></span>

## <a name="method-tablename"></a><span data-ttu-id="f53c3-385">メソッド tableName</span><span class="sxs-lookup"><span data-stu-id="f53c3-385">Method tableName</span></span>

<span data-ttu-id="f53c3-386">指定されたテーブルの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-386">Provides the name of a specified table.</span></span>

```xpp
public str tableName(TableId tableId)
```

### <a name="parameters---tablename"></a><span data-ttu-id="f53c3-387">パラメーター - tableName</span><span class="sxs-lookup"><span data-stu-id="f53c3-387">Parameters - tableName</span></span>

<span data-ttu-id="f53c3-388">tableId</span><span class="sxs-lookup"><span data-stu-id="f53c3-388">tableId</span></span>  
<span data-ttu-id="f53c3-389">テーブル ID を示す tableId システムのデータ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-389">A tableId system data type that indicates the table ID.</span></span>

### <a name="return-value---tablename"></a><span data-ttu-id="f53c3-390">戻り値 - tableName</span><span class="sxs-lookup"><span data-stu-id="f53c3-390">Return Value - tableName</span></span>

<span data-ttu-id="f53c3-391">テーブル名を示す文字列、存在しない tableId 値を渡すと UNKNOWN。</span><span class="sxs-lookup"><span data-stu-id="f53c3-391">A string that indicates the table name; UNKNOWN if you pass a tableId value that does not exist.</span></span>

### <a name="remarks---tablename"></a><span data-ttu-id="f53c3-392">備考 - tableName</span><span class="sxs-lookup"><span data-stu-id="f53c3-392">Remarks - tableName</span></span>

<span data-ttu-id="f53c3-393">存在しない tableId 値を渡すと、不明が返されます。</span><span class="sxs-lookup"><span data-stu-id="f53c3-393">The method returns UNKNOWN if you pass a tableId value that does not exist.</span></span>

## <a name="method-tablename2id"></a><span data-ttu-id="f53c3-394">メソッド tableName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-394">Method tableName2Id</span></span>

<span data-ttu-id="f53c3-395">テーブルの名前に基づいて、指定されたテーブルの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-395">Provides the ID for a specified table, based on the table name.</span></span>

```xpp
public TableId tableName2Id(str name)
```

### <a name="parameters---tablename2id"></a><span data-ttu-id="f53c3-396">パラメーター - tableName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-396">Parameters - tableName2Id</span></span>

<span data-ttu-id="f53c3-397">名前</span><span class="sxs-lookup"><span data-stu-id="f53c3-397">name</span></span>  
<span data-ttu-id="f53c3-398">テーブル名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-398">A string that indicates the table name.</span></span>

### <a name="return-value---tablename2id"></a><span data-ttu-id="f53c3-399">戻り値 - tableName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-399">Return Value - tableName2Id</span></span>

<span data-ttu-id="f53c3-400">テーブル ID を示す TableId システムのデータ型値、存在しないテーブルの名前の値を渡すと 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="f53c3-400">A tableId system data type value that indicates the table ID; 0 (zero) if you pass a name value for a nonexistent table.</span></span>

## <a name="method-tablenext"></a><span data-ttu-id="f53c3-401">メソッド tableNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-401">Method tableNext</span></span>

<span data-ttu-id="f53c3-402">テーブル ID に基づいて、指定されたテーブルの後に続くテーブルを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-402">Indicates the table that succeeds a specified table, based on the table IDs.</span></span>

```xpp
public TableId tableNext(TableId tableId)
```

### <a name="parameters---tablenext"></a><span data-ttu-id="f53c3-403">パラメーター - tableNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-403">Parameters - tableNext</span></span>

<span data-ttu-id="f53c3-404">tableId</span><span class="sxs-lookup"><span data-stu-id="f53c3-404">tableId</span></span>  
<span data-ttu-id="f53c3-405">テーブル ID を示す tableId システムのデータ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-405">A tableId system data type that indicates a table ID.</span></span>

### <a name="return-value---tablenext"></a><span data-ttu-id="f53c3-406">戻り値 - tableNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-406">Return Value - tableNext</span></span>

<span data-ttu-id="f53c3-407">指定されたテーブルの後に続くテーブルの TableId システムのデータ型値。</span><span class="sxs-lookup"><span data-stu-id="f53c3-407">A tableId system data type value for the table that succeeds the specified table.</span></span>

## <a name="method-tableobject"></a><span data-ttu-id="f53c3-408">メソッド tableObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-408">Method tableObject</span></span>

<span data-ttu-id="f53c3-409">DictTable オブジェクトを返すことで、指定されたテーブルに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-409">Provides information about a specified table by returning a DictTable object.</span></span>

```xpp
public DictTable tableObject(TableId tableId)
```

### <a name="parameters---tableobject"></a><span data-ttu-id="f53c3-410">パラメーター - tableObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-410">Parameters - tableObject</span></span>

<span data-ttu-id="f53c3-411">tableId</span><span class="sxs-lookup"><span data-stu-id="f53c3-411">tableId</span></span>  
<span data-ttu-id="f53c3-412">テーブル ID を示す tableId システムのデータ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-412">A tableId system data type that indicates a table ID.</span></span>

### <a name="return-value---tableobject"></a><span data-ttu-id="f53c3-413">戻り値 - tableObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-413">Return Value - tableObject</span></span>

<span data-ttu-id="f53c3-414">指定されたテーブルに関する情報を含む DictTable オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f53c3-414">A DictTable object that contains information about the specified table.</span></span>

## <a name="method-tablesql"></a><span data-ttu-id="f53c3-415">メソッド tableSql</span><span class="sxs-lookup"><span data-stu-id="f53c3-415">Method tableSql</span></span>

<span data-ttu-id="f53c3-416">テーブルが SQL テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-416">Indicates whether a table is a SQL table.</span></span>

```xpp
public boolean tableSql(TableId tableId)
```

### <a name="parameters---tablesql"></a><span data-ttu-id="f53c3-417">パラメーター - tableSql</span><span class="sxs-lookup"><span data-stu-id="f53c3-417">Parameters - tableSql</span></span>

<span data-ttu-id="f53c3-418">tableId</span><span class="sxs-lookup"><span data-stu-id="f53c3-418">tableId</span></span>  
<span data-ttu-id="f53c3-419">テーブル ID を示す tableId システムのデータ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-419">A tableId system data type that indicates the table ID.</span></span>

### <a name="return-value---tablesql"></a><span data-ttu-id="f53c3-420">戻り値 - tableSql</span><span class="sxs-lookup"><span data-stu-id="f53c3-420">Return Value - tableSql</span></span>

<span data-ttu-id="f53c3-421">テーブルが SQL テーブルである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f53c3-421">true if the table is a SQL table; otherwise, false.</span></span>

## <a name="method-tablesystem"></a><span data-ttu-id="f53c3-422">メソッド tableSystem</span><span class="sxs-lookup"><span data-stu-id="f53c3-422">Method tableSystem</span></span>

<span data-ttu-id="f53c3-423">テーブルがシステム テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-423">Indicates whether a table is a system table.</span></span>

```xpp
public boolean tableSystem(TableId tableId)
```

### <a name="parameters---tablesystem"></a><span data-ttu-id="f53c3-424">パラメーター - tableSystem</span><span class="sxs-lookup"><span data-stu-id="f53c3-424">Parameters - tableSystem</span></span>

<span data-ttu-id="f53c3-425">tableId</span><span class="sxs-lookup"><span data-stu-id="f53c3-425">tableId</span></span>  
<span data-ttu-id="f53c3-426">テーブル ID を示す tableId システムのデータ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-426">A tableId system data type that indicates a table ID.</span></span>

### <a name="return-value---tablesystem"></a><span data-ttu-id="f53c3-427">戻り値 - tableSystem</span><span class="sxs-lookup"><span data-stu-id="f53c3-427">Return Value - tableSystem</span></span>

<span data-ttu-id="f53c3-428">テーブルがシステム テーブルである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f53c3-428">true if the table is a system table; otherwise, false.</span></span>

### <a name="remarks---tablesystem"></a><span data-ttu-id="f53c3-429">備考 - tableSystem</span><span class="sxs-lookup"><span data-stu-id="f53c3-429">Remarks - tableSystem</span></span>

<span data-ttu-id="f53c3-430">tableNum 組み込み関数を使用して、テーブル ID の代わりにテーブル名をこのメソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="f53c3-430">You can pass a table name to this method instead of a table ID by using the tableNum intrinsic function.</span></span> <span data-ttu-id="f53c3-431">この機能の詳細については、「組み込み関数」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f53c3-431">For more information, see Intrinsic Functions.</span></span>

## <a name="method-testcode"></a><span data-ttu-id="f53c3-432">メソッド testCode</span><span class="sxs-lookup"><span data-stu-id="f53c3-432">Method testCode</span></span>

```xpp
public int testCode(int id, str value, str name, str serialno, str expiryDate, [int userCount], [boolean verifyCert], [str timestamp])
```

### <a name="parameters---testcode"></a><span data-ttu-id="f53c3-433">パラメーター - testCode</span><span class="sxs-lookup"><span data-stu-id="f53c3-433">Parameters - testCode</span></span>

<span data-ttu-id="f53c3-434">id</span><span class="sxs-lookup"><span data-stu-id="f53c3-434">id</span></span>  

<!-- -->

<span data-ttu-id="f53c3-435">値</span><span class="sxs-lookup"><span data-stu-id="f53c3-435">value</span></span>  

<!-- -->

<span data-ttu-id="f53c3-436">名前</span><span class="sxs-lookup"><span data-stu-id="f53c3-436">name</span></span>  

<!-- -->

<span data-ttu-id="f53c3-437">serialno</span><span class="sxs-lookup"><span data-stu-id="f53c3-437">serialno</span></span>  

<!-- -->

<span data-ttu-id="f53c3-438">expiryDate</span><span class="sxs-lookup"><span data-stu-id="f53c3-438">expiryDate</span></span>  

<!-- -->

<span data-ttu-id="f53c3-439">userCount</span><span class="sxs-lookup"><span data-stu-id="f53c3-439">userCount</span></span>  

<!-- -->

<span data-ttu-id="f53c3-440">verifyCert</span><span class="sxs-lookup"><span data-stu-id="f53c3-440">verifyCert</span></span>  

<!-- -->

<span data-ttu-id="f53c3-441">timestamp</span><span class="sxs-lookup"><span data-stu-id="f53c3-441">timestamp</span></span>  

### <a name="return-value---testcode"></a><span data-ttu-id="f53c3-442">戻り値 - testCode</span><span class="sxs-lookup"><span data-stu-id="f53c3-442">Return Value - testCode</span></span>

## <a name="method-typecnt"></a><span data-ttu-id="f53c3-443">メソッド typeCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-443">Method typeCnt</span></span>

<span data-ttu-id="f53c3-444">拡張データ型の数を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-444">Indicates the number of extended data types.</span></span>

```xpp
public int typeCnt()
```

### <a name="return-value---typecnt"></a><span data-ttu-id="f53c3-445">戻り値 - typeCnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-445">Return Value - typeCnt</span></span>

<span data-ttu-id="f53c3-446">拡張データ型の数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-446">An integer that indicates the number of extended data types.</span></span>

## <a name="method-typecnt2id"></a><span data-ttu-id="f53c3-447">メソッド typeCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-447">Method typeCnt2Id</span></span>

<span data-ttu-id="f53c3-448">指定された拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-448">Provides the ID of a specified extended data type.</span></span>

```xpp
public ExtendedTypeId typeCnt2Id(int cnt)
```

### <a name="parameters---typecnt2id"></a><span data-ttu-id="f53c3-449">パラメーター - typeCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-449">Parameters - typeCnt2Id</span></span>

<span data-ttu-id="f53c3-450">cnt</span><span class="sxs-lookup"><span data-stu-id="f53c3-450">cnt</span></span>  
<span data-ttu-id="f53c3-451">拡張データ型の順序に基づいて拡張データ型を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="f53c3-451">An integer that specifies an extended data type, based on the order of extended data types.</span></span>

### <a name="return-value---typecnt2id"></a><span data-ttu-id="f53c3-452">戻り値 - typeCnt2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-452">Return Value - typeCnt2Id</span></span>

<span data-ttu-id="f53c3-453">拡張データ型の ID を示す extendedTypeId システム データ型値です。Dictionary::typeCnt メソッドによって返される拡張データ型の数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="f53c3-453">An extendedTypeId system data type value that indicates the ID of the extended data type; 0 (zero) if you pass a cnt value that is larger than the number of extended data types that is returned by the Dictionary::typeCnt method.</span></span>

## <a name="method-typename"></a><span data-ttu-id="f53c3-454">メソッド typeName</span><span class="sxs-lookup"><span data-stu-id="f53c3-454">Method typeName</span></span>

<span data-ttu-id="f53c3-455">指定された拡張データ型の名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-455">Provides the name of a specified extended data type.</span></span>

```xpp
public str typeName(ExtendedTypeId typeId)
```

### <a name="parameters---typename"></a><span data-ttu-id="f53c3-456">パラメーター - typeName</span><span class="sxs-lookup"><span data-stu-id="f53c3-456">Parameters - typeName</span></span>

<span data-ttu-id="f53c3-457">typeId</span><span class="sxs-lookup"><span data-stu-id="f53c3-457">typeId</span></span>  
<span data-ttu-id="f53c3-458">拡張データ型の ID を示す extendedTypeId システム データ型です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-458">An extendedTypeId system data type that indicates the ID of an extended data type.</span></span>

### <a name="return-value---typename"></a><span data-ttu-id="f53c3-459">戻り値 - typeName</span><span class="sxs-lookup"><span data-stu-id="f53c3-459">Return Value - typeName</span></span>

<span data-ttu-id="f53c3-460">拡張データ型の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-460">A string that indicates the name of the extended data type.</span></span>

## <a name="method-typename2id"></a><span data-ttu-id="f53c3-461">メソッド typeName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-461">Method typeName2Id</span></span>

<span data-ttu-id="f53c3-462">拡張データ型名に基づいて、指定された拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-462">Provides the ID for a specified extended data type, based on the extended data type name.</span></span>

```xpp
public ExtendedTypeId typeName2Id(str name)
```

### <a name="parameters---typename2id"></a><span data-ttu-id="f53c3-463">パラメーター - typeName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-463">Parameters - typeName2Id</span></span>

<span data-ttu-id="f53c3-464">名前</span><span class="sxs-lookup"><span data-stu-id="f53c3-464">name</span></span>  
<span data-ttu-id="f53c3-465">拡張データ型の名前を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f53c3-465">A string that indicates the name of the extended data type.</span></span>

### <a name="return-value---typename2id"></a><span data-ttu-id="f53c3-466">戻り値 - typeName2Id</span><span class="sxs-lookup"><span data-stu-id="f53c3-466">Return Value - typeName2Id</span></span>

<span data-ttu-id="f53c3-467">拡張データ型の ID を示す extendedTypeId システム データ型値です。存在しない拡張データ型の名前の値を渡した場合は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="f53c3-467">An extendedTypeId system data type value that indicates the ID of the extended data type; 0 (zero) if you pass a name value for a nonexistent extended data type.</span></span>

## <a name="method-typenext"></a><span data-ttu-id="f53c3-468">メソッド typeNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-468">Method typeNext</span></span>

<span data-ttu-id="f53c3-469">ID に基づいて、指定された拡張データ型の後に続く拡張データ型を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-469">Indicates the extended data type that succeeds a specified extended data type, based on the IDs.</span></span>

```xpp
public ExtendedTypeId typeNext(ExtendedTypeId typeId)
```

### <a name="parameters---typenext"></a><span data-ttu-id="f53c3-470">パラメーター - typeNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-470">Parameters - typeNext</span></span>

<span data-ttu-id="f53c3-471">typeId</span><span class="sxs-lookup"><span data-stu-id="f53c3-471">typeId</span></span>  
<span data-ttu-id="f53c3-472">拡張データ型の ID を示す extendedTypeId システム データ型です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-472">An extendedTypeId system data type that indicates the ID for an extended data type.</span></span>

### <a name="return-value---typenext"></a><span data-ttu-id="f53c3-473">戻り値 - typeNext</span><span class="sxs-lookup"><span data-stu-id="f53c3-473">Return Value - typeNext</span></span>

<span data-ttu-id="f53c3-474">指定された拡張データ型を継承する拡張データ型の extendedTypeId システム データ型値です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-474">An extendedTypeId system data type value for the extended data type that succeeds the specified extended data type.</span></span>

## <a name="method-typeobject"></a><span data-ttu-id="f53c3-475">メソッド typeObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-475">Method typeObject</span></span>

<span data-ttu-id="f53c3-476">DictType オブジェクトを返すことで、指定された拡張データ型に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-476">Provides information about a specified extended data type by returning a DictType object.</span></span>

```xpp
public DictType typeObject(ExtendedTypeId typeId)
```

### <a name="parameters---typeobject"></a><span data-ttu-id="f53c3-477">パラメーター - typeObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-477">Parameters - typeObject</span></span>

<span data-ttu-id="f53c3-478">typeId</span><span class="sxs-lookup"><span data-stu-id="f53c3-478">typeId</span></span>  
<span data-ttu-id="f53c3-479">拡張データ型の ID を示す extendedTypeId システム データ型です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-479">An extendedTypeId system data type that indicates the ID for an extended data type.</span></span>

### <a name="return-value---typeobject"></a><span data-ttu-id="f53c3-480">戻り値 - typeObject</span><span class="sxs-lookup"><span data-stu-id="f53c3-480">Return Value - typeObject</span></span>

<span data-ttu-id="f53c3-481">指定されてた拡張データ型に関する情報を含む DictType オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f53c3-481">A DictType object that contains information about the specified extended data type.</span></span>

## <a name="method-safemode"></a><span data-ttu-id="f53c3-482">メソッド safeMode</span><span class="sxs-lookup"><span data-stu-id="f53c3-482">Method safeMode</span></span>

```xpp
public static boolean safeMode()
```

### <a name="return-value---safemode"></a><span data-ttu-id="f53c3-483">戻り値 - safeMode</span><span class="sxs-lookup"><span data-stu-id="f53c3-483">Return Value - safeMode</span></span>

## <a name="method-loginsettingsflush"></a><span data-ttu-id="f53c3-484">メソッド loginSettingsFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-484">Method loginSettingsFlush</span></span>

<span data-ttu-id="f53c3-485">ログオン設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-485">Refreshes the logon settings.</span></span>

```xpp
public static void loginSettingsFlush()
```

## <a name="method-dataflush"></a><span data-ttu-id="f53c3-486">メソッド dataFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-486">Method dataFlush</span></span>

<span data-ttu-id="f53c3-487">テーブル データを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-487">Refreshes the table data.</span></span>

```xpp
public static void dataFlush([TableId tableId])
```

### <a name="parameters---dataflush"></a><span data-ttu-id="f53c3-488">パラメーター - dataFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-488">Parameters - dataFlush</span></span>

<span data-ttu-id="f53c3-489">tableId</span><span class="sxs-lookup"><span data-stu-id="f53c3-489">tableId</span></span>  
<span data-ttu-id="f53c3-490">単一のテーブルまたはすべてのテーブルを示す tableId システムのデータ型。</span><span class="sxs-lookup"><span data-stu-id="f53c3-490">A tableId system data type that indicates a single table or all tables.</span></span> <span data-ttu-id="f53c3-491">既定値はすべてです。</span><span class="sxs-lookup"><span data-stu-id="f53c3-491">The default value is ALL.</span></span>

### <a name="remarks---dataflush"></a><span data-ttu-id="f53c3-492">備考 - dataFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-492">Remarks - dataFlush</span></span>

<span data-ttu-id="f53c3-493">既定では、このメソッドはすべてのテーブルのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-493">By default, this method refreshes data in all tables.</span></span>

## <a name="method-tableflush"></a><span data-ttu-id="f53c3-494">メソッド tableFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-494">Method tableFlush</span></span>

<span data-ttu-id="f53c3-495">テーブを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-495">Refreshes the tables.</span></span>

```xpp
public void tableFlush()
```

## <a name="method-enumflush"></a><span data-ttu-id="f53c3-496">メソッド enumFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-496">Method enumFlush</span></span>

<span data-ttu-id="f53c3-497">列挙型を更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-497">Refreshes the enumeration types.</span></span>

```xpp
public void enumFlush()
```

## <a name="method-new"></a><span data-ttu-id="f53c3-498">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f53c3-498">Method new</span></span>

<span data-ttu-id="f53c3-499">Dictionary クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-499">Initializes a new instance of the Dictionary class.</span></span>

```xpp
public void new()
```

## <a name="method-classflush"></a><span data-ttu-id="f53c3-500">メソッド classFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-500">Method classFlush</span></span>

<span data-ttu-id="f53c3-501">クラスを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-501">Refreshes the classes.</span></span>

```xpp
public void classFlush()
```

## <a name="method-reloadsecurity"></a><span data-ttu-id="f53c3-502">メソッド reloadSecurity</span><span class="sxs-lookup"><span data-stu-id="f53c3-502">Method reloadSecurity</span></span>

<span data-ttu-id="f53c3-503">機能キー システムを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="f53c3-503">Reloads the feature key system.</span></span>

```xpp
public void reloadSecurity([boolean reloadCodes], [boolean setSynchronizeRequired], [boolean flushTable])
```

### <a name="parameters---reloadsecurity"></a><span data-ttu-id="f53c3-504">パラメーター - reloadSecurity</span><span class="sxs-lookup"><span data-stu-id="f53c3-504">Parameters - reloadSecurity</span></span>

<span data-ttu-id="f53c3-505">reloadCodes</span><span class="sxs-lookup"><span data-stu-id="f53c3-505">reloadCodes</span></span>  

<!-- -->

<span data-ttu-id="f53c3-506">setSynchronizeRequired</span><span class="sxs-lookup"><span data-stu-id="f53c3-506">setSynchronizeRequired</span></span>  

<!-- -->

<span data-ttu-id="f53c3-507">flushTable</span><span class="sxs-lookup"><span data-stu-id="f53c3-507">flushTable</span></span>  

### <a name="remarks---reloadsecurity"></a><span data-ttu-id="f53c3-508">備考 - reloadSecurity</span><span class="sxs-lookup"><span data-stu-id="f53c3-508">Remarks - reloadSecurity</span></span>

<span data-ttu-id="f53c3-509">\_reloadCodes パラメーターの既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-509">The default value for the \_reloadCodes parameter is false.</span></span> <span data-ttu-id="f53c3-510">\_setSynchronizeRequired パラメーターの既定値は true です。</span><span class="sxs-lookup"><span data-stu-id="f53c3-510">The default value for the \_setSynchronizeRequired parameter is true.</span></span>

## <a name="method-typeflush"></a><span data-ttu-id="f53c3-511">メソッド typeFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-511">Method typeFlush</span></span>

<span data-ttu-id="f53c3-512">拡張データ型を更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-512">Refreshes the extended data types.</span></span>

```xpp
public void typeFlush()
```

## <a name="method-configurationkeyflush"></a><span data-ttu-id="f53c3-513">メソッド configurationKeyFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-513">Method configurationKeyFlush</span></span>

<span data-ttu-id="f53c3-514">コンフィギュレーション キーを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-514">Refreshes the configuration keys.</span></span>

```xpp
public void configurationKeyFlush()
```

## <a name="method-licensecodeflush"></a><span data-ttu-id="f53c3-515">メソッド licenseCodeFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-515">Method licenseCodeFlush</span></span>

<span data-ttu-id="f53c3-516">ライセンス コードを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-516">Refreshes the license codes.</span></span>

```xpp
public void licenseCodeFlush()
```

## <a name="method-aodflush"></a><span data-ttu-id="f53c3-517">メソッド aodFlush</span><span class="sxs-lookup"><span data-stu-id="f53c3-517">Method aodFlush</span></span>

<span data-ttu-id="f53c3-518">.aod ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53c3-518">Refreshes the .aod file.</span></span>

```xpp
public static void aodFlush()
```

