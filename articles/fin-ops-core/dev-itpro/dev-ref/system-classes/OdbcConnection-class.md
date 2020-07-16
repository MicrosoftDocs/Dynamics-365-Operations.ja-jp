---
title: OdbcConnection クラス
description: このトピックでは、OdbcConnection クラスについて説明します。
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
ms.openlocfilehash: cb342714ac876e546a1abb2e589ab274861aac2c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502562"
---
# <a name="class-odbcconnection"></a><span data-ttu-id="23328-103">クラス OdbcConnection</span><span class="sxs-lookup"><span data-stu-id="23328-103">Class OdbcConnection</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OdbcConnection extends Connection
```

<span data-ttu-id="23328-104">OdbcConnection クラスは、ODBC (Open Database Connectivity) を使用してデータベース接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="23328-104">The OdbcConnection class establishes a database connection by using ODBC (Open Database Connectivity).</span></span>

## <a name="remarks"></a><span data-ttu-id="23328-105">備考</span><span class="sxs-lookup"><span data-stu-id="23328-105">Remarks</span></span>

<span data-ttu-id="23328-106">OdbcConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="23328-106">In the context of an OdbcConnection instance, SQL statements are run, and results are returned.</span></span> <span data-ttu-id="23328-107">ODBC データ ソースへの接続を確立できない場合、例外がスローされ、その原因が Infolog に転記されます。</span><span class="sxs-lookup"><span data-stu-id="23328-107">If a connection to the ODBC data source cannot be established, an exception is thrown, and the reason is posted in the Infolog.</span></span> <span data-ttu-id="23328-108">このクラスは、正しい ODBC ドライバーがインストールされ、コントロール パネルの ODBC マネージャーで構成されている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="23328-108">This class works only if the correct ODBC drivers have been installed and configured in ODBC Manager in Control Panel.</span></span>

## <a name="examples"></a><span data-ttu-id="23328-109">例</span><span class="sxs-lookup"><span data-stu-id="23328-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="23328-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="23328-110">Methods</span></span>

| <span data-ttu-id="23328-111">方法</span><span class="sxs-lookup"><span data-stu-id="23328-111">Method</span></span>                               | <span data-ttu-id="23328-112">説明</span><span class="sxs-lookup"><span data-stu-id="23328-112">Description</span></span>                                                                                              |
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23328-113">public void new(LoginProperty Login)</span><span class="sxs-lookup"><span data-stu-id="23328-113">public void new(LoginProperty Login)</span></span> | <span data-ttu-id="23328-114">ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="23328-114">Establishes a connection to a data source, based on logon properties such as the user name and password.</span></span> |

## <a name="method-new"></a><span data-ttu-id="23328-115">メソッド new</span><span class="sxs-lookup"><span data-stu-id="23328-115">Method new</span></span>

<span data-ttu-id="23328-116">ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="23328-116">Establishes a connection to a data source, based on logon properties such as the user name and password.</span></span>

```xpp
public void new(LoginProperty Login)
```

### <a name="parameters---new"></a><span data-ttu-id="23328-117">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="23328-117">Parameters - new</span></span>

<span data-ttu-id="23328-118">ログイン</span><span class="sxs-lookup"><span data-stu-id="23328-118">Login</span></span>  
<span data-ttu-id="23328-119">ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="23328-119">A LoginProperty class instance that contains the user name, password, data source name, database, and so on.</span></span>

