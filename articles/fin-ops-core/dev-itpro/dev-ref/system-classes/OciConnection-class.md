---
title: OciConnection クラス
description: このトピックでは、OciConnection クラスについて説明します。
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
ms.openlocfilehash: 2d744906fb4ce90039e6f6b753cd26e1c2651f72
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502563"
---
# <a name="class-ociconnection"></a><span data-ttu-id="9eebf-103">クラス OciConnection</span><span class="sxs-lookup"><span data-stu-id="9eebf-103">Class OciConnection</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OciConnection extends Connection
```

<span data-ttu-id="9eebf-104">OciConnection クラスは、Oci (Oracle 呼び出しインターフェイス) を使用するデータベース接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="9eebf-104">The OciConnection class establishes a database connection that uses Oci (Oracle Call Interface).</span></span>

## <a name="remarks"></a><span data-ttu-id="9eebf-105">備考</span><span class="sxs-lookup"><span data-stu-id="9eebf-105">Remarks</span></span>

<span data-ttu-id="9eebf-106">OciConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="9eebf-106">In the context of an OciConnection instance, SQL statements are run, and results are returned.</span></span> <span data-ttu-id="9eebf-107">LoginProperty インスタンスに対して指定されている情報を基に、接続を確立できない場合、例外および理由は、情報ログに転記されます。</span><span class="sxs-lookup"><span data-stu-id="9eebf-107">If the connection cannot be established based on the information that is specified for the LoginProperty instance, an exception is thrown, and the reason is posted in the Infolog.</span></span> <span data-ttu-id="9eebf-108">このクラスは、Oracle クライアント ソフトウェアがインストールされている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9eebf-108">This class can be used only when Oracle client software is installed.</span></span>

## <a name="examples"></a><span data-ttu-id="9eebf-109">例</span><span class="sxs-lookup"><span data-stu-id="9eebf-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9eebf-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="9eebf-110">Methods</span></span>

| <span data-ttu-id="9eebf-111">方法</span><span class="sxs-lookup"><span data-stu-id="9eebf-111">Method</span></span>                               | <span data-ttu-id="9eebf-112">説明</span><span class="sxs-lookup"><span data-stu-id="9eebf-112">Description</span></span>                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eebf-113">public void new(LoginProperty Login)</span><span class="sxs-lookup"><span data-stu-id="9eebf-113">public void new(LoginProperty Login)</span></span> | <span data-ttu-id="9eebf-114">ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="9eebf-114">Establishes a connection to an Oracle database, based on logon properties such as the user name and password.</span></span> |

## <a name="method-new"></a><span data-ttu-id="9eebf-115">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9eebf-115">Method new</span></span>

<span data-ttu-id="9eebf-116">ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="9eebf-116">Establishes a connection to an Oracle database, based on logon properties such as the user name and password.</span></span>

```xpp
public void new(LoginProperty Login)
```

### <a name="parameters---new"></a><span data-ttu-id="9eebf-117">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="9eebf-117">Parameters - new</span></span>

<span data-ttu-id="9eebf-118">ログイン</span><span class="sxs-lookup"><span data-stu-id="9eebf-118">Login</span></span>  
<span data-ttu-id="9eebf-119">ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="9eebf-119">A LoginProperty class instance that contains the user name, password, data source name, database, and so on.</span></span>

