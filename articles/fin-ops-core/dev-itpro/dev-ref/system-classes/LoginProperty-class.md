---
title: LoginProperty クラス
description: このトピックでは、LoginProperty クラスについて説明します。
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
ms.openlocfilehash: 4d57ab7f86ebca9a01b22c50bc76a44a9bfbb01c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502890"
---
# <a name="class-loginproperty"></a><span data-ttu-id="89a29-103">クラス LoginProperty</span><span class="sxs-lookup"><span data-stu-id="89a29-103">Class LoginProperty</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class LoginProperty extends Object
```

<span data-ttu-id="89a29-104">LoginProperty クラスでは、OdbcConnection クラスのインスタンスにログオン情報を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="89a29-104">The LoginProperty class enables logon information to be passed to an instance of the OdbcConnection class.</span></span>

## <a name="remarks"></a><span data-ttu-id="89a29-105">備考</span><span class="sxs-lookup"><span data-stu-id="89a29-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="89a29-106">例</span><span class="sxs-lookup"><span data-stu-id="89a29-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="89a29-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="89a29-107">Methods</span></span>

| <span data-ttu-id="89a29-108">方法</span><span class="sxs-lookup"><span data-stu-id="89a29-108">Method</span></span>                                                | <span data-ttu-id="89a29-109">説明</span><span class="sxs-lookup"><span data-stu-id="89a29-109">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a29-110">public str getDatabase()</span><span class="sxs-lookup"><span data-stu-id="89a29-110">public str getDatabase()</span></span>                              | <span data-ttu-id="89a29-111">LoginProperty クラスに格納されている、データベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-111">Retrieves the name of the database, as stored in the LoginProperty class.</span></span>                                                                                                                              |
| <span data-ttu-id="89a29-112">public str getDSN()</span><span class="sxs-lookup"><span data-stu-id="89a29-112">public str getDSN()</span></span>                                   | <span data-ttu-id="89a29-113">LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-113">Retrieves the data source name (DSN) that is stored in the LoginProperty class.</span></span>                                                                                                                        |
| <span data-ttu-id="89a29-114">public str getOciServiceName()</span><span class="sxs-lookup"><span data-stu-id="89a29-114">public str getOciServiceName()</span></span>                        | <span data-ttu-id="89a29-115">LoginProperty クラスに格納されている Oracle サービス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-115">Retrieves the Oracle service name that is stored in the LoginProperty class.</span></span>                                                                                                                           |
| <span data-ttu-id="89a29-116">public str getOther()</span><span class="sxs-lookup"><span data-stu-id="89a29-116">public str getOther()</span></span>                                 | <span data-ttu-id="89a29-117">LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-117">Retrieves the additional logon parameters that are stored in the LoginProperty class.</span></span>                                                                                                                  |
| <span data-ttu-id="89a29-118">public str getServer()</span><span class="sxs-lookup"><span data-stu-id="89a29-118">public str getServer()</span></span>                                | <span data-ttu-id="89a29-119">LoginProperty クラスに格納されているサーバー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-119">Retrieves the server name that is stored in the LoginProperty class.</span></span>                                                                                                                                   |
| <span data-ttu-id="89a29-120">public str getTcpIpPort()</span><span class="sxs-lookup"><span data-stu-id="89a29-120">public str getTcpIpPort()</span></span>                             | <span data-ttu-id="89a29-121">LoginProperty クラスに格納されている TCP/IP ポートを取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-121">Retrieves the TCP/IP port that is stored in the LoginProperty class.</span></span>                                                                                                                                   |
| <span data-ttu-id="89a29-122">public boolean getUsePredefinedService()</span><span class="sxs-lookup"><span data-stu-id="89a29-122">public boolean getUsePredefinedService()</span></span>              | <span data-ttu-id="89a29-123">loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="89a29-123">Returns whether the loginProperty class is set to use a predefined Oracle service instead of specifying the server and database information on the loginProperty class.</span></span>                                |
| <span data-ttu-id="89a29-124">public void setTcpIpPort(str tcpipPort)</span><span class="sxs-lookup"><span data-stu-id="89a29-124">public void setTcpIpPort(str tcpipPort)</span></span>               | <span data-ttu-id="89a29-125">Oracle に接続するために使用される TCP/IP ポートを指定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-125">Specifies which TCP/IP port is used to connect to Oracle.</span></span>                                                                                                                                              |
| <span data-ttu-id="89a29-126">public void setDatabase(str database)</span><span class="sxs-lookup"><span data-stu-id="89a29-126">public void setDatabase(str database)</span></span>                 | <span data-ttu-id="89a29-127">ログイン先のデータベースの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-127">Sets the name of the database to log on to.</span></span>                                                                                                                                                            |
| <span data-ttu-id="89a29-128">public void setDSN(str datasourceName)</span><span class="sxs-lookup"><span data-stu-id="89a29-128">public void setDSN(str datasourceName)</span></span>                | <span data-ttu-id="89a29-129">データ ソースへのアクセスに使用される DSN を設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-129">Sets the DSN that is used to access the data source.</span></span>                                                                                                                                                   |
| <span data-ttu-id="89a29-130">public void new()</span><span class="sxs-lookup"><span data-stu-id="89a29-130">public void new()</span></span>                                     | <span data-ttu-id="89a29-131">LoginProperty クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89a29-131">Initializes a new instance of the LoginProperty class.</span></span>                                                                                                                                                 |
| <span data-ttu-id="89a29-132">public void setOciServiceName(str ociServiceName)</span><span class="sxs-lookup"><span data-stu-id="89a29-132">public void setOciServiceName(str ociServiceName)</span></span>     | <span data-ttu-id="89a29-133">Oracle サービス名を指定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-133">Specifies an Oracle service name.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="89a29-134">public void setOther(str otherOdbcParameters)</span><span class="sxs-lookup"><span data-stu-id="89a29-134">public void setOther(str otherOdbcParameters)</span></span>         | <span data-ttu-id="89a29-135">LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-135">Sets additional nonstandard logon parameters that are stored in the LoginProperty class.</span></span>                                                                                                               |
| <span data-ttu-id="89a29-136">public void setServer(str serverName)</span><span class="sxs-lookup"><span data-stu-id="89a29-136">public void setServer(str serverName)</span></span>                 | <span data-ttu-id="89a29-137">データベースが置かれているサーバーの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-137">Sets the name of the server on which the database resides.</span></span>                                                                                                                                             |
| <span data-ttu-id="89a29-138">public void setUsePredefinedService(boolean newValue)</span><span class="sxs-lookup"><span data-stu-id="89a29-138">public void setUsePredefinedService(boolean newValue)</span></span> | <span data-ttu-id="89a29-139">接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-139">Specifies whether to use a predefined Oracle service (created by using Oracle network configuration tools) for the connection information, or whether it will be specified in the loginProperty class.</span></span> |

## <a name="method-getdatabase"></a><span data-ttu-id="89a29-140">メソッド getDatabase</span><span class="sxs-lookup"><span data-stu-id="89a29-140">Method getDatabase</span></span>

<span data-ttu-id="89a29-141">LoginProperty クラスに格納されている、データベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-141">Retrieves the name of the database, as stored in the LoginProperty class.</span></span>

```xpp
public str getDatabase()
```

### <a name="return-value---getdatabase"></a><span data-ttu-id="89a29-142">戻り値 - getDatabase</span><span class="sxs-lookup"><span data-stu-id="89a29-142">Return Value - getDatabase</span></span>

<span data-ttu-id="89a29-143">データベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="89a29-143">The name of the database.</span></span>

## <a name="method-getdsn"></a><span data-ttu-id="89a29-144">メソッド getDSN</span><span class="sxs-lookup"><span data-stu-id="89a29-144">Method getDSN</span></span>

<span data-ttu-id="89a29-145">LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-145">Retrieves the data source name (DSN) that is stored in the LoginProperty class.</span></span>

```xpp
public str getDSN()
```

### <a name="return-value---getdsn"></a><span data-ttu-id="89a29-146">戻り値 - getDSN</span><span class="sxs-lookup"><span data-stu-id="89a29-146">Return Value - getDSN</span></span>

<span data-ttu-id="89a29-147">DSN。</span><span class="sxs-lookup"><span data-stu-id="89a29-147">The DSN.</span></span>

## <a name="method-getociservicename"></a><span data-ttu-id="89a29-148">メソッド getOciServiceName</span><span class="sxs-lookup"><span data-stu-id="89a29-148">Method getOciServiceName</span></span>

<span data-ttu-id="89a29-149">LoginProperty クラスに格納されている Oracle サービス名を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-149">Retrieves the Oracle service name that is stored in the LoginProperty class.</span></span>

```xpp
public str getOciServiceName()
```

### <a name="return-value---getociservicename"></a><span data-ttu-id="89a29-150">戻り値 - getOciServiceName</span><span class="sxs-lookup"><span data-stu-id="89a29-150">Return Value - getOciServiceName</span></span>

<span data-ttu-id="89a29-151">Oracle サービス名。</span><span class="sxs-lookup"><span data-stu-id="89a29-151">The Oracle service name.</span></span>

## <a name="method-getother"></a><span data-ttu-id="89a29-152">メソッド getOther</span><span class="sxs-lookup"><span data-stu-id="89a29-152">Method getOther</span></span>

<span data-ttu-id="89a29-153">LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-153">Retrieves the additional logon parameters that are stored in the LoginProperty class.</span></span>

```xpp
public str getOther()
```

### <a name="return-value---getother"></a><span data-ttu-id="89a29-154">戻り値 - getOther</span><span class="sxs-lookup"><span data-stu-id="89a29-154">Return Value - getOther</span></span>

<span data-ttu-id="89a29-155">文字列としての追加ログオン パラメーター。</span><span class="sxs-lookup"><span data-stu-id="89a29-155">The additional logon parameters as a string.</span></span>

## <a name="method-getserver"></a><span data-ttu-id="89a29-156">メソッド getServer</span><span class="sxs-lookup"><span data-stu-id="89a29-156">Method getServer</span></span>

<span data-ttu-id="89a29-157">LoginProperty クラスに格納されているサーバー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-157">Retrieves the server name that is stored in the LoginProperty class.</span></span>

```xpp
public str getServer()
```

### <a name="return-value---getserver"></a><span data-ttu-id="89a29-158">戻り値 - getServer</span><span class="sxs-lookup"><span data-stu-id="89a29-158">Return Value - getServer</span></span>

<span data-ttu-id="89a29-159">サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="89a29-159">The name of the server.</span></span>

## <a name="method-gettcpipport"></a><span data-ttu-id="89a29-160">メソッド getTcpIpPort</span><span class="sxs-lookup"><span data-stu-id="89a29-160">Method getTcpIpPort</span></span>

<span data-ttu-id="89a29-161">LoginProperty クラスに格納されている TCP/IP ポートを取得します。</span><span class="sxs-lookup"><span data-stu-id="89a29-161">Retrieves the TCP/IP port that is stored in the LoginProperty class.</span></span>

```xpp
public str getTcpIpPort()
```

### <a name="return-value---gettcpipport"></a><span data-ttu-id="89a29-162">戻り値 - getTcpIpPort</span><span class="sxs-lookup"><span data-stu-id="89a29-162">Return Value - getTcpIpPort</span></span>

<span data-ttu-id="89a29-163">TCP/IP ポート。</span><span class="sxs-lookup"><span data-stu-id="89a29-163">The TCP/IP port.</span></span>

## <a name="method-getusepredefinedservice"></a><span data-ttu-id="89a29-164">メソッド getUsePredefinedService</span><span class="sxs-lookup"><span data-stu-id="89a29-164">Method getUsePredefinedService</span></span>

<span data-ttu-id="89a29-165">loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。</span><span class="sxs-lookup"><span data-stu-id="89a29-165">Returns whether the loginProperty class is set to use a predefined Oracle service instead of specifying the server and database information on the loginProperty class.</span></span>

```xpp
public boolean getUsePredefinedService()
```

### <a name="return-value---getusepredefinedservice"></a><span data-ttu-id="89a29-166">戻り値 - getUsePredefinedService</span><span class="sxs-lookup"><span data-stu-id="89a29-166">Return Value - getUsePredefinedService</span></span>

<span data-ttu-id="89a29-167">定義済みの Oracle サービスが接続に使用される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="89a29-167">true if a predefined Oracle service is used to connect; otherwise, false.</span></span>

## <a name="method-settcpipport"></a><span data-ttu-id="89a29-168">メソッド setTcpIpPort</span><span class="sxs-lookup"><span data-stu-id="89a29-168">Method setTcpIpPort</span></span>

<span data-ttu-id="89a29-169">Oracle に接続するために使用される TCP/IP ポートを指定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-169">Specifies which TCP/IP port is used to connect to Oracle.</span></span>

```xpp
public void setTcpIpPort(str tcpipPort)
```

### <a name="parameters---settcpipport"></a><span data-ttu-id="89a29-170">パラメーター - setTcpIpPort</span><span class="sxs-lookup"><span data-stu-id="89a29-170">Parameters - setTcpIpPort</span></span>

<span data-ttu-id="89a29-171">tcpipPort</span><span class="sxs-lookup"><span data-stu-id="89a29-171">tcpipPort</span></span>  
<span data-ttu-id="89a29-172">使用する TCP/IP ポート。</span><span class="sxs-lookup"><span data-stu-id="89a29-172">The TCP/IP port to use.</span></span>

### <a name="remarks---settcpipport"></a><span data-ttu-id="89a29-173">備考 - setTcpIpPort</span><span class="sxs-lookup"><span data-stu-id="89a29-173">Remarks - setTcpIpPort</span></span>

<span data-ttu-id="89a29-174">既定のポートは 1521 です。</span><span class="sxs-lookup"><span data-stu-id="89a29-174">The default port is 1521.</span></span>

## <a name="method-setdatabase"></a><span data-ttu-id="89a29-175">メソッド setDatabase</span><span class="sxs-lookup"><span data-stu-id="89a29-175">Method setDatabase</span></span>

<span data-ttu-id="89a29-176">ログイン先のデータベースの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-176">Sets the name of the database to log on to.</span></span>

```xpp
public void setDatabase(str database)
```

### <a name="parameters---setdatabase"></a><span data-ttu-id="89a29-177">パラメーター - setDatabase</span><span class="sxs-lookup"><span data-stu-id="89a29-177">Parameters - setDatabase</span></span>

<span data-ttu-id="89a29-178">データベース</span><span class="sxs-lookup"><span data-stu-id="89a29-178">database</span></span>  
<span data-ttu-id="89a29-179">データベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="89a29-179">The name of the database.</span></span>

## <a name="method-setdsn"></a><span data-ttu-id="89a29-180">メソッド setDSN</span><span class="sxs-lookup"><span data-stu-id="89a29-180">Method setDSN</span></span>

<span data-ttu-id="89a29-181">データ ソースへのアクセスに使用される DSN を設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-181">Sets the DSN that is used to access the data source.</span></span>

```xpp
public void setDSN(str datasourceName)
```

### <a name="parameters---setdsn"></a><span data-ttu-id="89a29-182">パラメーター - setDSN</span><span class="sxs-lookup"><span data-stu-id="89a29-182">Parameters - setDSN</span></span>

<span data-ttu-id="89a29-183">datasourceName</span><span class="sxs-lookup"><span data-stu-id="89a29-183">datasourceName</span></span>  
<span data-ttu-id="89a29-184">データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="89a29-184">The name of the data source.</span></span>

## <a name="method-new"></a><span data-ttu-id="89a29-185">メソッド new</span><span class="sxs-lookup"><span data-stu-id="89a29-185">Method new</span></span>

<span data-ttu-id="89a29-186">LoginProperty クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="89a29-186">Initializes a new instance of the LoginProperty class.</span></span>

```xpp
public void new()
```

## <a name="method-setociservicename"></a><span data-ttu-id="89a29-187">メソッド setOciServiceName</span><span class="sxs-lookup"><span data-stu-id="89a29-187">Method setOciServiceName</span></span>

<span data-ttu-id="89a29-188">Oracle サービス名を指定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-188">Specifies an Oracle service name.</span></span>

```xpp
public void setOciServiceName(str ociServiceName)
```

### <a name="parameters---setociservicename"></a><span data-ttu-id="89a29-189">パラメーター - setOciServiceName</span><span class="sxs-lookup"><span data-stu-id="89a29-189">Parameters - setOciServiceName</span></span>

<span data-ttu-id="89a29-190">ociServiceName</span><span class="sxs-lookup"><span data-stu-id="89a29-190">ociServiceName</span></span>  
<span data-ttu-id="89a29-191">サービスの名前。</span><span class="sxs-lookup"><span data-stu-id="89a29-191">The name of the service.</span></span>

### <a name="remarks---setociservicename"></a><span data-ttu-id="89a29-192">備考 - setOciServiceName</span><span class="sxs-lookup"><span data-stu-id="89a29-192">Remarks - setOciServiceName</span></span>

<span data-ttu-id="89a29-193">このメソッドは、loginProperty クラスが事前定義済みの Oracle サービスを使用するように設定されていない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="89a29-193">This method is used when the loginProperty class is not set to use a predefined Oracle service.</span></span>

## <a name="method-setother"></a><span data-ttu-id="89a29-194">メソッド setOther</span><span class="sxs-lookup"><span data-stu-id="89a29-194">Method setOther</span></span>

<span data-ttu-id="89a29-195">LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-195">Sets additional nonstandard logon parameters that are stored in the LoginProperty class.</span></span>

```xpp
public void setOther(str otherOdbcParameters)
```

### <a name="parameters---setother"></a><span data-ttu-id="89a29-196">パラメーター - setOther</span><span class="sxs-lookup"><span data-stu-id="89a29-196">Parameters - setOther</span></span>

<span data-ttu-id="89a29-197">otherOdbcParameters</span><span class="sxs-lookup"><span data-stu-id="89a29-197">otherOdbcParameters</span></span>  
<span data-ttu-id="89a29-198">ODBC 書式に設定された追加のパラメータ。</span><span class="sxs-lookup"><span data-stu-id="89a29-198">The additional ODBC-formatted parameters.</span></span>

### <a name="remarks---setother"></a><span data-ttu-id="89a29-199">備考 - setOther</span><span class="sxs-lookup"><span data-stu-id="89a29-199">Remarks - setOther</span></span>

<span data-ttu-id="89a29-200">このメソッドは、使用するデータソースに追加の非標準のパラメーターが必要な場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="89a29-200">This method should be used only if the data source that you want to use requires some additional, nonstandard parameters.</span></span> <span data-ttu-id="89a29-201">パラメーターは、標準の ODBC 形式の &lt;parm1&gt;=&lt;value1&gt;;&lt;parm2&gt;=&lt;value2&gt; で、たとえば、MODE=1;PATCH=32 で適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89a29-201">The parameters must be applied in the standard ODBC format: &lt;parm1&gt;=&lt;value1&gt;;&lt;parm2&gt;=&lt;value2&gt;,... For example: MODE=1;PATCH=32</span></span>

## <a name="method-setserver"></a><span data-ttu-id="89a29-202">メソッド setServer</span><span class="sxs-lookup"><span data-stu-id="89a29-202">Method setServer</span></span>

<span data-ttu-id="89a29-203">データベースが置かれているサーバーの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-203">Sets the name of the server on which the database resides.</span></span>

```xpp
public void setServer(str serverName)
```

### <a name="parameters---setserver"></a><span data-ttu-id="89a29-204">パラメーター - setServer</span><span class="sxs-lookup"><span data-stu-id="89a29-204">Parameters - setServer</span></span>

<span data-ttu-id="89a29-205">serverName</span><span class="sxs-lookup"><span data-stu-id="89a29-205">serverName</span></span>  
<span data-ttu-id="89a29-206">データベースがあるサーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="89a29-206">The name of the server where the database is located.</span></span>

## <a name="method-setusepredefinedservice"></a><span data-ttu-id="89a29-207">メソッド setUsePredefinedService</span><span class="sxs-lookup"><span data-stu-id="89a29-207">Method setUsePredefinedService</span></span>

<span data-ttu-id="89a29-208">接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="89a29-208">Specifies whether to use a predefined Oracle service (created by using Oracle network configuration tools) for the connection information, or whether it will be specified in the loginProperty class.</span></span>

```xpp
public void setUsePredefinedService(boolean newValue)
```

### <a name="parameters---setusepredefinedservice"></a><span data-ttu-id="89a29-209">パラメーター - setUsePredefinedService</span><span class="sxs-lookup"><span data-stu-id="89a29-209">Parameters - setUsePredefinedService</span></span>

<span data-ttu-id="89a29-210">newValue</span><span class="sxs-lookup"><span data-stu-id="89a29-210">newValue</span></span>  
<span data-ttu-id="89a29-211">事前定義された Oracle サービスを使用するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="89a29-211">A Boolean value that indicates whether to use a predefined Oracle service.</span></span>

### <a name="remarks---setusepredefinedservice"></a><span data-ttu-id="89a29-212">備考 - setUsePredefinedService</span><span class="sxs-lookup"><span data-stu-id="89a29-212">Remarks - setUsePredefinedService</span></span>

<span data-ttu-id="89a29-213">既定では、事前に定義されたサービスは使用されません。</span><span class="sxs-lookup"><span data-stu-id="89a29-213">By default, a predefined service is not used.</span></span>


