---
title: MapiMessage クラス
description: このトピックでは、MapiMessage クラスについて説明します。
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
ms.openlocfilehash: 1f00f6d5bbd880e8f5c8ff69ab94eaeee85ae948
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502579"
---
# <a name="class-mapimessage"></a><span data-ttu-id="a9bf1-103">クラス MapiMessage</span><span class="sxs-lookup"><span data-stu-id="a9bf1-103">Class MapiMessage</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapiMessage extends Object
```

<span data-ttu-id="a9bf1-104">MapiMessage クラスには、MAPI システムから送受信されるメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-104">The MapiMessage class contains a message that is sent to or received from the MAPI system.</span></span> <span data-ttu-id="a9bf1-105">メッセージには、件名、テキスト、受信者情報、および添付ファイル情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-105">The message includes a subject, text, recipient information, and attachment information.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9bf1-106">備考</span><span class="sxs-lookup"><span data-stu-id="a9bf1-106">Remarks</span></span>

<span data-ttu-id="a9bf1-107">メッセージを送受信するとき、メッセージは、MapiMessage対象として MAPI システムとの間を渡されます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-107">When you send or receive a message, the message is passed to and from the MAPI system as a MapiMessage object.</span></span>

## <a name="examples"></a><span data-ttu-id="a9bf1-108">例</span><span class="sxs-lookup"><span data-stu-id="a9bf1-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a9bf1-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="a9bf1-109">Methods</span></span>

| <span data-ttu-id="a9bf1-110">方法</span><span class="sxs-lookup"><span data-stu-id="a9bf1-110">Method</span></span>                                                        | <span data-ttu-id="a9bf1-111">説明</span><span class="sxs-lookup"><span data-stu-id="a9bf1-111">Description</span></span>                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bf1-112">public str conversationID(\[str conversationId\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-112">public str conversationID(\[str conversationId\])</span></span>             | <span data-ttu-id="a9bf1-113">メッセージが所属する会話スレッドを識別する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-113">Gets or sets the string that identifies the conversation thread to which the message belongs.</span></span>           |
| <span data-ttu-id="a9bf1-114">public str dateReceived(\[Date theDate\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-114">public str dateReceived(\[Date theDate\])</span></span>                     | <span data-ttu-id="a9bf1-115">メッセージを受信した日付を返します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-115">Returns the date when the message was received.</span></span>                                                         |
| <span data-ttu-id="a9bf1-116">public int flags(\[int flags\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-116">public int flags(\[int flags\])</span></span>                               | <span data-ttu-id="a9bf1-117">メッセージ ステータス フラグのビットを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-117">Set or get a bitmask of the message status flags.</span></span>                                                       |
| <span data-ttu-id="a9bf1-118">public MapiFileDesc getFileNo(int fileNo)</span><span class="sxs-lookup"><span data-stu-id="a9bf1-118">public MapiFileDesc getFileNo(int fileNo)</span></span>                     | <span data-ttu-id="a9bf1-119">メッセージからの添付ファイルを取得します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-119">Gets a file attachment from a message.</span></span>                                                                  |
| <span data-ttu-id="a9bf1-120">public MapiRecipDesc getRecipNo(int recipientNo)</span><span class="sxs-lookup"><span data-stu-id="a9bf1-120">public MapiRecipDesc getRecipNo(int recipientNo)</span></span>               | <span data-ttu-id="a9bf1-121">MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-121">Retrieves information about a message recipient in a MapiRecipDesc object.</span></span>                              |
| <span data-ttu-id="a9bf1-122">public str messageType(\[str messageType\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-122">public str messageType(\[str messageType\])</span></span>                   | <span data-ttu-id="a9bf1-123">IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-123">Gets or sets the string that indicates that the message is not of the IPM (interpersonal message) type.</span></span> |
| <span data-ttu-id="a9bf1-124">public int numFiles(\[int numFiles\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-124">public int numFiles(\[int numFiles\])</span></span>                         |                                                                                                         |
| <span data-ttu-id="a9bf1-125">public int numRecips(\[int numRecips\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-125">public int numRecips(\[int numRecips\])</span></span>                       |                                                                                                         |
| <span data-ttu-id="a9bf1-126">public MapiRecipDesc originator(\[MapiRecipDesc originator\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-126">public MapiRecipDesc originator(\[MapiRecipDesc originator\])</span></span> |                                                                                                         |
| <span data-ttu-id="a9bf1-127">public str subject(\[str subject\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-127">public str subject(\[str subject\])</span></span>                           |                                                                                                         |
| <span data-ttu-id="a9bf1-128">public str text(\[str text\])</span><span class="sxs-lookup"><span data-stu-id="a9bf1-128">public str text(\[str text\])</span></span>                                 |                                                                                                         |
| <span data-ttu-id="a9bf1-129">public void new()</span><span class="sxs-lookup"><span data-stu-id="a9bf1-129">public void new()</span></span>                                             | <span data-ttu-id="a9bf1-130">MapiMessage クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-130">Initializes an instance of the MapiMessage class.</span></span>                                                       |
| <span data-ttu-id="a9bf1-131">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="a9bf1-131">public void finalize()</span></span>                                        |                                                                                                         |
| <span data-ttu-id="a9bf1-132">public void setRecipNo(int recipNo, MapiRecipDesc recipient)</span><span class="sxs-lookup"><span data-stu-id="a9bf1-132">public void setRecipNo(int recipNo, MapiRecipDesc recipient)</span></span>  | <span data-ttu-id="a9bf1-133">メッセージに受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-133">Adds a recipient to the message.</span></span>                                                                        |
| <span data-ttu-id="a9bf1-134">public void setFileNo(int fileNo, MapiFileDesc file)</span><span class="sxs-lookup"><span data-stu-id="a9bf1-134">public void setFileNo(int fileNo, MapiFileDesc file)</span></span>          | <span data-ttu-id="a9bf1-135">メッセージの添付ファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-135">Sets a file attachment for the message.</span></span>                                                                 |

## <a name="method-conversationid"></a><span data-ttu-id="a9bf1-136">メソッド conversationID</span><span class="sxs-lookup"><span data-stu-id="a9bf1-136">Method conversationID</span></span>

<span data-ttu-id="a9bf1-137">メッセージが所属する会話スレッドを識別する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-137">Gets or sets the string that identifies the conversation thread to which the message belongs.</span></span>

```xpp
public str conversationID([str conversationId])
```

### <a name="parameters---conversationid"></a><span data-ttu-id="a9bf1-138">パラメーター - conversationID</span><span class="sxs-lookup"><span data-stu-id="a9bf1-138">Parameters - conversationID</span></span>

<span data-ttu-id="a9bf1-139">conversationId</span><span class="sxs-lookup"><span data-stu-id="a9bf1-139">conversationId</span></span>  
<span data-ttu-id="a9bf1-140">会話スレッドの ID。省略可能。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-140">The ID of the conversation thread; optional.</span></span>

### <a name="return-value---conversationid"></a><span data-ttu-id="a9bf1-141">戻り値 - conversationID</span><span class="sxs-lookup"><span data-stu-id="a9bf1-141">Return Value - conversationID</span></span>

<span data-ttu-id="a9bf1-142">メッセージが所属する会話スレッドを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-142">A string that identifies the conversation thread to which the message belongs.</span></span>

### <a name="remarks---conversationid"></a><span data-ttu-id="a9bf1-143">備考 - conversationID</span><span class="sxs-lookup"><span data-stu-id="a9bf1-143">Remarks - conversationID</span></span>

<span data-ttu-id="a9bf1-144">メッセージング システムの中には、無視してこのメンバーを返さないものがあります。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-144">Some messaging systems might ignore and not return this member.</span></span>

## <a name="method-datereceived"></a><span data-ttu-id="a9bf1-145">メソッド dateReceived</span><span class="sxs-lookup"><span data-stu-id="a9bf1-145">Method dateReceived</span></span>

<span data-ttu-id="a9bf1-146">メッセージを受信した日付を返します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-146">Returns the date when the message was received.</span></span>

```xpp
public str dateReceived([Date theDate])
```

### <a name="parameters---datereceived"></a><span data-ttu-id="a9bf1-147">パラメーター - dateReceived</span><span class="sxs-lookup"><span data-stu-id="a9bf1-147">Parameters - dateReceived</span></span>

<span data-ttu-id="a9bf1-148">theDate</span><span class="sxs-lookup"><span data-stu-id="a9bf1-148">theDate</span></span>  
<span data-ttu-id="a9bf1-149">メッセージを受信した日付 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-149">The date when the message was received; optional.</span></span>

### <a name="return-value---datereceived"></a><span data-ttu-id="a9bf1-150">戻り値 - dateReceived</span><span class="sxs-lookup"><span data-stu-id="a9bf1-150">Return Value - dateReceived</span></span>

<span data-ttu-id="a9bf1-151">メッセージが受信された日付を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-151">A string that indicates the date when the message was received.</span></span>

### <a name="remarks---datereceived"></a><span data-ttu-id="a9bf1-152">備考 - dateReceived</span><span class="sxs-lookup"><span data-stu-id="a9bf1-152">Remarks - dateReceived</span></span>

<span data-ttu-id="a9bf1-153">返される文字列の形式は、YYYY/MM/DD HH:MMであり、24時間制を使用します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-153">The format of the string that is returned is YYYY/MM/DD HH:MM and uses a 24-hour clock.</span></span>

## <a name="method-flags"></a><span data-ttu-id="a9bf1-154">メソッド flags</span><span class="sxs-lookup"><span data-stu-id="a9bf1-154">Method flags</span></span>

<span data-ttu-id="a9bf1-155">メッセージ ステータス フラグのビットを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-155">Set or get a bitmask of the message status flags.</span></span>

```xpp
public int flags([int flags])
```

### <a name="parameters---flags"></a><span data-ttu-id="a9bf1-156">パラメーター - flags</span><span class="sxs-lookup"><span data-stu-id="a9bf1-156">Parameters - flags</span></span>

<span data-ttu-id="a9bf1-157">flags</span><span class="sxs-lookup"><span data-stu-id="a9bf1-157">flags</span></span>  
<span data-ttu-id="a9bf1-158">メッセージ ステータス フラグ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-158">The message status flags; optional.</span></span>

### <a name="return-value---flags"></a><span data-ttu-id="a9bf1-159">戻り値 - flags</span><span class="sxs-lookup"><span data-stu-id="a9bf1-159">Return Value - flags</span></span>

<span data-ttu-id="a9bf1-160">メッセージ ステータス フラグのビット。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-160">A bitmask of the message status flags.</span></span>

### <a name="remarks---flags"></a><span data-ttu-id="a9bf1-161">備考 - flags</span><span class="sxs-lookup"><span data-stu-id="a9bf1-161">Remarks - flags</span></span>

<span data-ttu-id="a9bf1-162">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-162">The following flags can be set:</span></span>

-   <span data-ttu-id="a9bf1-163">\#MAPI\_RECEIPT\_REQUESTED � 受領通知のリクエストが要求されました。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-163">\#MAPI\_RECEIPT\_REQUESTED � Receipt notification is requested.</span></span> <span data-ttu-id="a9bf1-164">クライアント アプリケーションは、メッセージを送信するときにこのビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-164">Client applications set this bit when they send a message.</span></span>
-   <span data-ttu-id="a9bf1-165">\#MAPI\_SENT � メッセージが送信されました。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-165">\#MAPI\_SENT � The message has been sent.</span></span>
-   <span data-ttu-id="a9bf1-166">\#MAPI\_UNREAD � メッセージが未読です。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-166">\#MAPI\_UNREAD � The message has not been read.</span></span>

## <a name="method-getfileno"></a><span data-ttu-id="a9bf1-167">メソッド getFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-167">Method getFileNo</span></span>

<span data-ttu-id="a9bf1-168">メッセージからの添付ファイルを取得します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-168">Gets a file attachment from a message.</span></span>

```xpp
public MapiFileDesc getFileNo(int fileNo)
```

### <a name="parameters---getfileno"></a><span data-ttu-id="a9bf1-169">パラメーター - getFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-169">Parameters - getFileNo</span></span>

<span data-ttu-id="a9bf1-170">fileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-170">fileNo</span></span>  
<span data-ttu-id="a9bf1-171">取得する添付ファイルのインデックス。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-171">The index of the attachment to retrieve.</span></span> <span data-ttu-id="a9bf1-172">インデックスは 1 から始まり、numFiles メソッドを使用して添付ファイルの総数を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-172">The index starts at 1, and the total number of attachments can be retrieved using the numFiles method.</span></span>

### <a name="return-value---getfileno"></a><span data-ttu-id="a9bf1-173">戻り値 - getFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-173">Return Value - getFileNo</span></span>

<span data-ttu-id="a9bf1-174">添付ファイルに関する情報を含む MapiFileDesc オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-174">Returns a MapiFileDesc object that contains information about the attachment.</span></span>

### <a name="remarks---getfileno"></a><span data-ttu-id="a9bf1-175">備考 - getFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-175">Remarks - getFileNo</span></span>

<span data-ttu-id="a9bf1-176">添付ファイルは、MapiFileDesc オブジェクトで返されます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-176">The attached file is returned in a MapiFileDesc object.</span></span>

### <a name="examples---getfileno"></a><span data-ttu-id="a9bf1-177">例 - getFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-177">Examples - getFileNo</span></span>

```xpp
{ 
    MapiFileDesc attachment; 
    MapiMessage message; 
    // Retrieve message. 
    // ...  
    if (message.NumFiles() >= 1) 
    { 
        attachment = message.GetFileNo(1); 
    } 
}
```

## <a name="method-getrecipno"></a><span data-ttu-id="a9bf1-178">メソッド getRecipNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-178">Method getRecipNo</span></span>

<span data-ttu-id="a9bf1-179">MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-179">Retrieves information about a message recipient in a MapiRecipDesc object.</span></span>

```xpp
public MapiRecipDesc getRecipNo(int recipientNo)
```

### <a name="parameters---getrecipno"></a><span data-ttu-id="a9bf1-180">パラメーター - getRecipNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-180">Parameters - getRecipNo</span></span>

<span data-ttu-id="a9bf1-181">recipientNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-181">recipientNo</span></span>  
<span data-ttu-id="a9bf1-182">取得する受信者の番号。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-182">The number of the recipient to retrieve.</span></span> <span data-ttu-id="a9bf1-183">番号付けは 1 から始まり、numRecips メソッドを使用して受信者の総数を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-183">The numbering starts at 1, and the total number of recipients can be read by using the numRecips method.</span></span>

### <a name="return-value---getrecipno"></a><span data-ttu-id="a9bf1-184">戻り値 - getRecipNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-184">Return Value - getRecipNo</span></span>

<span data-ttu-id="a9bf1-185">受信者または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を説明する MapiRecipDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-185">A MapiRecipDesc object that describes the recipient or nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

## <a name="method-messagetype"></a><span data-ttu-id="a9bf1-186">メソッド messageType</span><span class="sxs-lookup"><span data-stu-id="a9bf1-186">Method messageType</span></span>

<span data-ttu-id="a9bf1-187">IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-187">Gets or sets the string that indicates that the message is not of the IPM (interpersonal message) type.</span></span>

```xpp
public str messageType([str messageType])
```

### <a name="parameters---messagetype"></a><span data-ttu-id="a9bf1-188">パラメーター - messageType</span><span class="sxs-lookup"><span data-stu-id="a9bf1-188">Parameters - messageType</span></span>

<span data-ttu-id="a9bf1-189">messageType</span><span class="sxs-lookup"><span data-stu-id="a9bf1-189">messageType</span></span>  
<span data-ttu-id="a9bf1-190">メッセージに設定する messageType 値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-190">The messageType value to set for the message; optional.</span></span>

### <a name="return-value---messagetype"></a><span data-ttu-id="a9bf1-191">戻り値 - messageType</span><span class="sxs-lookup"><span data-stu-id="a9bf1-191">Return Value - messageType</span></span>

<span data-ttu-id="a9bf1-192">messagetype 文字列。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-192">A messagetype string.</span></span>

### <a name="remarks---messagetype"></a><span data-ttu-id="a9bf1-193">備考 - messageType</span><span class="sxs-lookup"><span data-stu-id="a9bf1-193">Remarks - messageType</span></span>

<span data-ttu-id="a9bf1-194">アプリケーションは、IPM ではないメッセージのメッセージ タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-194">Applications can select message types for messages that are not IPMs.</span></span> <span data-ttu-id="a9bf1-195">IPM だけをサポートするクライアントは、メッセージを読むときに MessageType メンバーを無視し、メッセージを送信するときに空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-195">Clients that support only IPMs can ignore the MessageType member when they read messages and set it to empty when they send messages.</span></span>

## <a name="method-numfiles"></a><span data-ttu-id="a9bf1-196">メソッド numFiles</span><span class="sxs-lookup"><span data-stu-id="a9bf1-196">Method numFiles</span></span>

```xpp
public int numFiles([int numFiles])
```

### <a name="parameters---numfiles"></a><span data-ttu-id="a9bf1-197">パラメーター - numFiles</span><span class="sxs-lookup"><span data-stu-id="a9bf1-197">Parameters - numFiles</span></span>

<span data-ttu-id="a9bf1-198">numFiles</span><span class="sxs-lookup"><span data-stu-id="a9bf1-198">numFiles</span></span>  

### <a name="return-value---numfiles"></a><span data-ttu-id="a9bf1-199">戻り値 - numFiles</span><span class="sxs-lookup"><span data-stu-id="a9bf1-199">Return Value - numFiles</span></span>

## <a name="method-numrecips"></a><span data-ttu-id="a9bf1-200">メソッド numRecips</span><span class="sxs-lookup"><span data-stu-id="a9bf1-200">Method numRecips</span></span>

```xpp
public int numRecips([int numRecips])
```

### <a name="parameters---numrecips"></a><span data-ttu-id="a9bf1-201">パラメーター - numRecips</span><span class="sxs-lookup"><span data-stu-id="a9bf1-201">Parameters - numRecips</span></span>

<span data-ttu-id="a9bf1-202">numRecips</span><span class="sxs-lookup"><span data-stu-id="a9bf1-202">numRecips</span></span>  

### <a name="return-value---numrecips"></a><span data-ttu-id="a9bf1-203">戻り値 - numRecips</span><span class="sxs-lookup"><span data-stu-id="a9bf1-203">Return Value - numRecips</span></span>

## <a name="method-originator"></a><span data-ttu-id="a9bf1-204">メソッド originator</span><span class="sxs-lookup"><span data-stu-id="a9bf1-204">Method originator</span></span>

```xpp
public MapiRecipDesc originator([MapiRecipDesc originator])
```

### <a name="parameters---originator"></a><span data-ttu-id="a9bf1-205">パラメーター - originator</span><span class="sxs-lookup"><span data-stu-id="a9bf1-205">Parameters - originator</span></span>

<span data-ttu-id="a9bf1-206">originator</span><span class="sxs-lookup"><span data-stu-id="a9bf1-206">originator</span></span>  

### <a name="return-value---originator"></a><span data-ttu-id="a9bf1-207">戻り値 - originator</span><span class="sxs-lookup"><span data-stu-id="a9bf1-207">Return Value - originator</span></span>

## <a name="method-subject"></a><span data-ttu-id="a9bf1-208">メソッド subject</span><span class="sxs-lookup"><span data-stu-id="a9bf1-208">Method subject</span></span>

```xpp
public str subject([str subject])
```

### <a name="parameters---subject"></a><span data-ttu-id="a9bf1-209">パラメーター - subject</span><span class="sxs-lookup"><span data-stu-id="a9bf1-209">Parameters - subject</span></span>

<span data-ttu-id="a9bf1-210">subject</span><span class="sxs-lookup"><span data-stu-id="a9bf1-210">subject</span></span>  

### <a name="return-value---subject"></a><span data-ttu-id="a9bf1-211">戻り値 - subject</span><span class="sxs-lookup"><span data-stu-id="a9bf1-211">Return Value - subject</span></span>

## <a name="method-text"></a><span data-ttu-id="a9bf1-212">メソッド text</span><span class="sxs-lookup"><span data-stu-id="a9bf1-212">Method text</span></span>

```xpp
public str text([str text])
```

### <a name="parameters---text"></a><span data-ttu-id="a9bf1-213">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="a9bf1-213">Parameters - text</span></span>

<span data-ttu-id="a9bf1-214">テキスト</span><span class="sxs-lookup"><span data-stu-id="a9bf1-214">text</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="a9bf1-215">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="a9bf1-215">Return Value - text</span></span>

## <a name="method-new"></a><span data-ttu-id="a9bf1-216">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a9bf1-216">Method new</span></span>

<span data-ttu-id="a9bf1-217">MapiMessage クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-217">Initializes an instance of the MapiMessage class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="a9bf1-218">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="a9bf1-218">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-setrecipno"></a><span data-ttu-id="a9bf1-219">メソッド setRecipNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-219">Method setRecipNo</span></span>

<span data-ttu-id="a9bf1-220">メッセージに受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-220">Adds a recipient to the message.</span></span>

```xpp
public void setRecipNo(int recipNo, MapiRecipDesc recipient)
```

### <a name="parameters---setrecipno"></a><span data-ttu-id="a9bf1-221">パラメーター - setRecipNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-221">Parameters - setRecipNo</span></span>

<span data-ttu-id="a9bf1-222">recipNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-222">recipNo</span></span>  
<span data-ttu-id="a9bf1-223">受信者を説明する MapiRecipDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-223">The MapiRecipDesc object that describes the recipient.</span></span>

<!-- -->

<span data-ttu-id="a9bf1-224">recipient</span><span class="sxs-lookup"><span data-stu-id="a9bf1-224">recipient</span></span>  
<span data-ttu-id="a9bf1-225">受信者を説明する MapiRecipDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-225">The MapiRecipDesc object that describes the recipient.</span></span>

### <a name="remarks---setrecipno"></a><span data-ttu-id="a9bf1-226">備考 - setRecipNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-226">Remarks - setRecipNo</span></span>

<span data-ttu-id="a9bf1-227">正しい MapiRecipDesc オブジェクトをユーザーが入力した名前から取得する必要がある場合は、resolveName メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-227">If you have to get a correct MapiRecipDesc object from a name that a user entered, use the resolveName method.</span></span>

## <a name="method-setfileno"></a><span data-ttu-id="a9bf1-228">メソッド setFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-228">Method setFileNo</span></span>

<span data-ttu-id="a9bf1-229">メッセージの添付ファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-229">Sets a file attachment for the message.</span></span>

```xpp
public void setFileNo(int fileNo, MapiFileDesc file)
```

### <a name="parameters---setfileno"></a><span data-ttu-id="a9bf1-230">パラメーター - setFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-230">Parameters - setFileNo</span></span>

<span data-ttu-id="a9bf1-231">fileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-231">fileNo</span></span>  
<span data-ttu-id="a9bf1-232">添付ファイルを説明する MapiFileDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-232">The MapiFileDesc object that describes the attachment.</span></span>

<!-- -->

<span data-ttu-id="a9bf1-233">ファイル</span><span class="sxs-lookup"><span data-stu-id="a9bf1-233">file</span></span>  
<span data-ttu-id="a9bf1-234">添付ファイルを説明する MapiFileDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-234">The MapiFileDesc object that describes the attachment.</span></span>

### <a name="remarks---setfileno"></a><span data-ttu-id="a9bf1-235">備考 - setFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-235">Remarks - setFileNo</span></span>

<span data-ttu-id="a9bf1-236">添付ファイルには、1 から始まる番号が付けられます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-236">The attachments are numbered from 1.</span></span> <span data-ttu-id="a9bf1-237">したがって、最初の添付ファイルには番号 1 を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-237">Therefore, the first attachment should be numbered 1.</span></span> <span data-ttu-id="a9bf1-238">numFiles メソッドを呼び出してアタッチメントの数を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="a9bf1-238">You can call the numFiles method to retrieve the number of attachments.</span></span>

### <a name="examples---setfileno"></a><span data-ttu-id="a9bf1-239">例 - setFileNo</span><span class="sxs-lookup"><span data-stu-id="a9bf1-239">Examples - setFileNo</span></span>

```xpp
{ 
    MapiMessage msg = new MapiMessage(); 
    MapiFileDesc attachment = new MapiFileDesc(); 
    attachment.Path("C:\\files\\info.txt"); 
    msg.SetFileNo(1,attachment); 
}
```

