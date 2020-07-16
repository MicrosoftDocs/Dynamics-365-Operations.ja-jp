---
title: Mapi クラス
description: このトピックでは、Mapi クラスについて説明します。
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
ms.openlocfilehash: a98fdc0ff1735e4458eb9885b66212f1144a7392
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502588"
---
# <a name="class-mapi"></a><span data-ttu-id="0d5d3-103">クラス Mapi</span><span class="sxs-lookup"><span data-stu-id="0d5d3-103">Class Mapi</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Mapi extends Object
```

<span data-ttu-id="0d5d3-104">Mapi クラスを使用すると、Microsoft Exchange ベースのシステム、Microsoft Outlook Express、Lotus CCMail などのほとんどの主要なメール システムで、メールを送信、受信、管理できます。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-104">The Mapi class enables email to be sent, received, and managed in most major mail systems, such as Microsoft Exchange�based systems, Microsoft Outlook Express, and Lotus CCMail.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5d3-105">備考</span><span class="sxs-lookup"><span data-stu-id="0d5d3-105">Remarks</span></span>

<span data-ttu-id="0d5d3-106">他の Mapi クラス、MapiMessage、MapiRecipDesc、MapiFileDesc とともに、このクラスでは、複数の受信者、添付ファイル、メッセージ テキスト、件名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-106">Together with the other Mapi classes, MapiMessage, MapiRecipDesc, and MapiFileDesc, this class lets you specify multiple recipients, file attachments, message text, and a subject.</span></span> <span data-ttu-id="0d5d3-107">最も簡単な方法は、マシン上に作業用のメール クライアントを設定し、いくつかの電子メール メッセージを送受信することによって正しく動作することを確認することです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-107">The easiest approach is to set up a working mail client on the machine, and make sure that this works correctly order by sending and receiving a few email messages.</span></span> <span data-ttu-id="0d5d3-108">Mapi メソッドのフラグは、Mapi マクロに配置されます。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-108">Flags for the Mapi methods are located in the Mapi macro.</span></span> <span data-ttu-id="0d5d3-109">\#MAPI ステートメントと共に Mapi クラスを使用するコードにこのマクロを含めます。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-109">You include this macro in code where you use the Mapi classes together with the \#MAPI statement.</span></span>

## <a name="examples"></a><span data-ttu-id="0d5d3-110">例</span><span class="sxs-lookup"><span data-stu-id="0d5d3-110">Examples</span></span>

<span data-ttu-id="0d5d3-111">次の例は、このクラスを使用して電子メール メッセージを送信する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-111">The following example shows how to send an email message by using this class.</span></span>

```xpp
static void example() 
{ 
    #Mapi 
    Mapi m = new Mapi(); 
    MapiMessage msg = new MapiMessage(); 
    MapiRecipDesc recip = new MapiRecipDesc(); 
    // Set up the recipient. 
    recip.Name("someone"); 
    recip.RecipClass(#MAPI_TO); 
    msg.setRecipNo(1,recip); 
    // Log on using default profile. 
    m.Logon("","",#MAPI_USE_DEFAULT); 
    // Send the mail, and allow the user to modify the 
    // Subject, Text and Recipients in the Send Mail Dialog. 
    m.SendMail(msg,#MAPI_DIALOG); 
    // Log off. 
    m.Logoff(); 
}
```

## <a name="methods"></a><span data-ttu-id="0d5d3-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="0d5d3-112">Methods</span></span>

| <span data-ttu-id="0d5d3-113">方法</span><span class="sxs-lookup"><span data-stu-id="0d5d3-113">Method</span></span>                                                                         | <span data-ttu-id="0d5d3-114">説明</span><span class="sxs-lookup"><span data-stu-id="0d5d3-114">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5d3-115">public int deleteMail(str messageID)</span><span class="sxs-lookup"><span data-stu-id="0d5d3-115">public int deleteMail(str messageID)</span></span>                                           | <span data-ttu-id="0d5d3-116">メッセージ ストアから指定されたメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-116">Removes the specified message from the message store.</span></span>                                                |
| <span data-ttu-id="0d5d3-117">public str findNext(\[str messageType\], \[str seedMessageID\], \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="0d5d3-117">public str findNext(\[str messageType\], \[str seedMessageID\], \[int flags\])</span></span> | <span data-ttu-id="0d5d3-118">メッセージ店舗で最初または次のメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-118">Finds the first or next message in the message store.</span></span>                                                |
| <span data-ttu-id="0d5d3-119">public int logoff()</span><span class="sxs-lookup"><span data-stu-id="0d5d3-119">public int logoff()</span></span>                                                            | <span data-ttu-id="0d5d3-120">メール システムからログオフすることができます。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-120">Lets you log off the mail system.</span></span>                                                                    |
| <span data-ttu-id="0d5d3-121">public int logon(str profileName, str password, int flags)</span><span class="sxs-lookup"><span data-stu-id="0d5d3-121">public int logon(str profileName, str password, int flags)</span></span>                     | <span data-ttu-id="0d5d3-122">指定されたプロファイルとパスワードを使用して、メール システムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-122">Logs on to the mail system by using the specified profile and password.</span></span>                              |
| <span data-ttu-id="0d5d3-123">public MapiMessage readMail(str messageID, \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="0d5d3-123">public MapiMessage readMail(str messageID, \[int flags\])</span></span>                      | <span data-ttu-id="0d5d3-124">メッセージ ストアからメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-124">Retrieves a message from the message store.</span></span>                                                          |
| <span data-ttu-id="0d5d3-125">public MapiRecipDesc resolveName(str mame, int flags)</span><span class="sxs-lookup"><span data-stu-id="0d5d3-125">public MapiRecipDesc resolveName(str mame, int flags)</span></span>                          | <span data-ttu-id="0d5d3-126">ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-126">Transforms the message recipient's name, as entered by a user, to an unambiguous address list entry.</span></span> |
| <span data-ttu-id="0d5d3-127">public int saveMail(MapiMessage message, int flags, str messageId)</span><span class="sxs-lookup"><span data-stu-id="0d5d3-127">public int saveMail(MapiMessage message, int flags, str messageId)</span></span>             | <span data-ttu-id="0d5d3-128">メッセージ ストアにメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-128">Saves a message to the message store.</span></span>                                                                |
| <span data-ttu-id="0d5d3-129">public int sendMail(MapiMessage message, \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="0d5d3-129">public int sendMail(MapiMessage message, \[int flags\])</span></span>                        | <span data-ttu-id="0d5d3-130">特定の受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-130">Sends a message to the specified recipients.</span></span>                                                         |
| <span data-ttu-id="0d5d3-131">public int status()</span><span class="sxs-lookup"><span data-stu-id="0d5d3-131">public int status()</span></span>                                                            | <span data-ttu-id="0d5d3-132">最後の Mapi 操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-132">Retrieves the status of the last Mapi operation.</span></span>                                                     |
| <span data-ttu-id="0d5d3-133">public void new()</span><span class="sxs-lookup"><span data-stu-id="0d5d3-133">public void new()</span></span>                                                              | <span data-ttu-id="0d5d3-134">Mapi クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-134">Initializes an instance of the Mapi class.</span></span>                                                           |
| <span data-ttu-id="0d5d3-135">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="0d5d3-135">public void finalize()</span></span>                                                         |                                                                                                      |

## <a name="method-deletemail"></a><span data-ttu-id="0d5d3-136">メソッド deleteMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-136">Method deleteMail</span></span>

<span data-ttu-id="0d5d3-137">メッセージ ストアから指定されたメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-137">Removes the specified message from the message store.</span></span>

```xpp
public int deleteMail(str messageID)
```

### <a name="parameters---deletemail"></a><span data-ttu-id="0d5d3-138">パラメーター - deleteMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-138">Parameters - deleteMail</span></span>

<span data-ttu-id="0d5d3-139">messageID</span><span class="sxs-lookup"><span data-stu-id="0d5d3-139">messageID</span></span>  
<span data-ttu-id="0d5d3-140">削除するメッセージの一意のメッセージ ID。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-140">The unique message ID for the message to delete.</span></span>

### <a name="return-value---deletemail"></a><span data-ttu-id="0d5d3-141">戻り値 - deleteMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-141">Return Value - deleteMail</span></span>

<span data-ttu-id="0d5d3-142">状態 \#SUCCESS\_SUCCES またはエラー コード。これは \#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-142">The status \#SUCCESS\_SUCCES or an error code, which can be found in the \#MAPI macro.</span></span>

### <a name="remarks---deletemail"></a><span data-ttu-id="0d5d3-143">備考 - deleteMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-143">Remarks - deleteMail</span></span>

<span data-ttu-id="0d5d3-144">メッセージ ID は、findNext メソッドを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-144">The message ID can be retrieved by using the findNext method.</span></span>

## <a name="method-findnext"></a><span data-ttu-id="0d5d3-145">メソッド findNext</span><span class="sxs-lookup"><span data-stu-id="0d5d3-145">Method findNext</span></span>

<span data-ttu-id="0d5d3-146">メッセージ店舗で最初または次のメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-146">Finds the first or next message in the message store.</span></span>

```xpp
public str findNext([str messageType], [str seedMessageID], [int flags])
```

### <a name="parameters---findnext"></a><span data-ttu-id="0d5d3-147">パラメーター - findNext</span><span class="sxs-lookup"><span data-stu-id="0d5d3-147">Parameters - findNext</span></span>

<span data-ttu-id="0d5d3-148">messageType</span><span class="sxs-lookup"><span data-stu-id="0d5d3-148">messageType</span></span>  
<span data-ttu-id="0d5d3-149">先入れ先出し (FIFO) を示すフラグまたは未読; オプション。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-149">Flags that indicate first in, first out (FIFO) or unread; optional.</span></span> <span data-ttu-id="0d5d3-150">このパラメーターには、次の 2 つの値があります。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-150">This parameter has two possible values:</span></span>

<!-- -->

<span data-ttu-id="0d5d3-151">seedMessageID</span><span class="sxs-lookup"><span data-stu-id="0d5d3-151">seedMessageID</span></span>  
<span data-ttu-id="0d5d3-152">先入れ先出し (FIFO) を示すフラグまたは未読; オプション。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-152">Flags that indicate first in, first out (FIFO) or unread; optional.</span></span> <span data-ttu-id="0d5d3-153">このパラメーターには、次の 2 つの値があります。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-153">This parameter has two possible values:</span></span>

<!-- -->

<span data-ttu-id="0d5d3-154">flags</span><span class="sxs-lookup"><span data-stu-id="0d5d3-154">flags</span></span>  
<span data-ttu-id="0d5d3-155">先入れ先出し (FIFO) を示すフラグまたは未読; オプション。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-155">Flags that indicate first in, first out (FIFO) or unread; optional.</span></span> <span data-ttu-id="0d5d3-156">このパラメーターには、次の 2 つの値があります。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-156">This parameter has two possible values:</span></span>

### <a name="return-value---findnext"></a><span data-ttu-id="0d5d3-157">戻り値 - findNext</span><span class="sxs-lookup"><span data-stu-id="0d5d3-157">Return Value - findNext</span></span>

<span data-ttu-id="0d5d3-158">見つかったメッセージのメッセージ ID。メッセージが見つからない場合は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-158">The message ID of the message that is found; an empty string if no message is found.</span></span>

### <a name="remarks---findnext"></a><span data-ttu-id="0d5d3-159">備考 - findNext</span><span class="sxs-lookup"><span data-stu-id="0d5d3-159">Remarks - findNext</span></span>

<span data-ttu-id="0d5d3-160">このメソッドを呼び出して最初のメッセージを検索し、続く呼び出しを発行して次のメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-160">Call this method to find the first message, and then issue subsequent calls to obtain the following messages.</span></span> <span data-ttu-id="0d5d3-161">このメソッドを呼び出した後、status メソッドを使用して Mapi エラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-161">Use the status method to check for Mapi errors after you call this method.</span></span>

## <a name="method-logoff"></a><span data-ttu-id="0d5d3-162">メソッド logoff</span><span class="sxs-lookup"><span data-stu-id="0d5d3-162">Method logoff</span></span>

<span data-ttu-id="0d5d3-163">メール システムからログオフすることができます。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-163">Lets you log off the mail system.</span></span>

```xpp
public int logoff()
```

### <a name="return-value---logoff"></a><span data-ttu-id="0d5d3-164">戻り値 - logoff</span><span class="sxs-lookup"><span data-stu-id="0d5d3-164">Return Value - logoff</span></span>

<span data-ttu-id="0d5d3-165">状態 \#SUCCESS\_SUCCESS またはエラー コード。これは \#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-165">The status \#SUCCESS\_SUCCESS or an error code, which can be found in the \#MAPI macro.</span></span>

## <a name="method-logon"></a><span data-ttu-id="0d5d3-166">メソッド logon</span><span class="sxs-lookup"><span data-stu-id="0d5d3-166">Method logon</span></span>

<span data-ttu-id="0d5d3-167">指定されたプロファイルとパスワードを使用して、メール システムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-167">Logs on to the mail system by using the specified profile and password.</span></span>

```xpp
public int logon(str profileName, str password, int flags)
```

### <a name="parameters---logon"></a><span data-ttu-id="0d5d3-168">パラメーター - logon</span><span class="sxs-lookup"><span data-stu-id="0d5d3-168">Parameters - logon</span></span>

<span data-ttu-id="0d5d3-169">profileName</span><span class="sxs-lookup"><span data-stu-id="0d5d3-169">profileName</span></span>  
<span data-ttu-id="0d5d3-170">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-170">A list of flags.</span></span> <span data-ttu-id="0d5d3-171">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-171">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="0d5d3-172">パスワード</span><span class="sxs-lookup"><span data-stu-id="0d5d3-172">password</span></span>  
<span data-ttu-id="0d5d3-173">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-173">A list of flags.</span></span> <span data-ttu-id="0d5d3-174">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-174">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="0d5d3-175">flags</span><span class="sxs-lookup"><span data-stu-id="0d5d3-175">flags</span></span>  
<span data-ttu-id="0d5d3-176">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-176">A list of flags.</span></span> <span data-ttu-id="0d5d3-177">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-177">The valid flags are as follows:</span></span>

### <a name="return-value---logon"></a><span data-ttu-id="0d5d3-178">戻り値 - logon</span><span class="sxs-lookup"><span data-stu-id="0d5d3-178">Return Value - logon</span></span>

<span data-ttu-id="0d5d3-179">ログオンに成功した場合は、状態 \#SUCCESS\_SUCCESS です。そうでない場合は、エラー コードを返します。これは、\#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-179">The status \#SUCCESS\_SUCCESS if the logon succeeded; otherwise, an error code, which can be found in the \#MAPI macro.</span></span>

### <a name="remarks---logon"></a><span data-ttu-id="0d5d3-180">備考 - logon</span><span class="sxs-lookup"><span data-stu-id="0d5d3-180">Remarks - logon</span></span>

<span data-ttu-id="0d5d3-181">ログオンするための簡単で一般的な方法は、既定のプロファイルを使用してログオンする \#MAPI\_USE\_DEFAULT フラグを指定することです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-181">An easy and common way to log on is to specify the \#MAPI\_USE\_DEFAULT flag, which logs on by using the default profile.</span></span>

## <a name="method-readmail"></a><span data-ttu-id="0d5d3-182">メソッド readMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-182">Method readMail</span></span>

<span data-ttu-id="0d5d3-183">メッセージ ストアからメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-183">Retrieves a message from the message store.</span></span>

```xpp
public MapiMessage readMail(str messageID, [int flags])
```

### <a name="parameters---readmail"></a><span data-ttu-id="0d5d3-184">パラメーター - readMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-184">Parameters - readMail</span></span>

<span data-ttu-id="0d5d3-185">messageID</span><span class="sxs-lookup"><span data-stu-id="0d5d3-185">messageID</span></span>  
<span data-ttu-id="0d5d3-186">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-186">A list of flags; optional.</span></span> <span data-ttu-id="0d5d3-187">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-187">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="0d5d3-188">flags</span><span class="sxs-lookup"><span data-stu-id="0d5d3-188">flags</span></span>  
<span data-ttu-id="0d5d3-189">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-189">A list of flags; optional.</span></span> <span data-ttu-id="0d5d3-190">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-190">The valid flags are as follows:</span></span>

### <a name="return-value---readmail"></a><span data-ttu-id="0d5d3-191">戻り値-readMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-191">Return Value - readMail</span></span>

<span data-ttu-id="0d5d3-192">取得された MapiMessage オブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-192">The MapiMessage object that is retrieved or nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

## <a name="method-resolvename"></a><span data-ttu-id="0d5d3-193">メソッド resolveName</span><span class="sxs-lookup"><span data-stu-id="0d5d3-193">Method resolveName</span></span>

<span data-ttu-id="0d5d3-194">ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-194">Transforms the message recipient's name, as entered by a user, to an unambiguous address list entry.</span></span>

```xpp
public MapiRecipDesc resolveName(str mame, int flags)
```

### <a name="parameters---resolvename"></a><span data-ttu-id="0d5d3-195">パラメーター - resolveName</span><span class="sxs-lookup"><span data-stu-id="0d5d3-195">Parameters - resolveName</span></span>

<span data-ttu-id="0d5d3-196">mame</span><span class="sxs-lookup"><span data-stu-id="0d5d3-196">mame</span></span>  
<span data-ttu-id="0d5d3-197">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-197">A list of flags.</span></span> <span data-ttu-id="0d5d3-198">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-198">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="0d5d3-199">flags</span><span class="sxs-lookup"><span data-stu-id="0d5d3-199">flags</span></span>  
<span data-ttu-id="0d5d3-200">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-200">A list of flags.</span></span> <span data-ttu-id="0d5d3-201">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-201">The valid flags are as follows:</span></span>

### <a name="return-value---resolvename"></a><span data-ttu-id="0d5d3-202">戻り値 - resolveName</span><span class="sxs-lookup"><span data-stu-id="0d5d3-202">Return Value - resolveName</span></span>

<span data-ttu-id="0d5d3-203">明確なアドレス一覧エントリを持つ MapiRecipDesc クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-203">A MapiRecipDesc class object that has an unambiguous address list entry.</span></span>

## <a name="method-savemail"></a><span data-ttu-id="0d5d3-204">メソッド saveMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-204">Method saveMail</span></span>

<span data-ttu-id="0d5d3-205">メッセージ ストアにメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-205">Saves a message to the message store.</span></span>

```xpp
public int saveMail(MapiMessage message, int flags, str messageId)
```

### <a name="parameters---savemail"></a><span data-ttu-id="0d5d3-206">パラメーター - saveMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-206">Parameters - saveMail</span></span>

<span data-ttu-id="0d5d3-207">メッセージ</span><span class="sxs-lookup"><span data-stu-id="0d5d3-207">message</span></span>  
<span data-ttu-id="0d5d3-208">取得するメッセージの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-208">The unique ID of the message to retrieve.</span></span>

<!-- -->

<span data-ttu-id="0d5d3-209">flags</span><span class="sxs-lookup"><span data-stu-id="0d5d3-209">flags</span></span>  
<span data-ttu-id="0d5d3-210">取得するメッセージの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-210">The unique ID of the message to retrieve.</span></span>

<!-- -->

<span data-ttu-id="0d5d3-211">messageId</span><span class="sxs-lookup"><span data-stu-id="0d5d3-211">messageId</span></span>  
<span data-ttu-id="0d5d3-212">取得するメッセージの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-212">The unique ID of the message to retrieve.</span></span>

### <a name="return-value---savemail"></a><span data-ttu-id="0d5d3-213">戻り値 - saveMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-213">Return Value - saveMail</span></span>

<span data-ttu-id="0d5d3-214">状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-214">The status \#SUCCESS\_SUCCESS or an error code from the \#MAPI macro.</span></span>

## <a name="method-sendmail"></a><span data-ttu-id="0d5d3-215">メソッド sendMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-215">Method sendMail</span></span>

<span data-ttu-id="0d5d3-216">特定の受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-216">Sends a message to the specified recipients.</span></span>

```xpp
public int sendMail(MapiMessage message, [int flags])
```

### <a name="parameters---sendmail"></a><span data-ttu-id="0d5d3-217">パラメーター - sendMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-217">Parameters - sendMail</span></span>

<span data-ttu-id="0d5d3-218">メッセージ</span><span class="sxs-lookup"><span data-stu-id="0d5d3-218">message</span></span>  
<span data-ttu-id="0d5d3-219">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-219">A list of flags; optional.</span></span> <span data-ttu-id="0d5d3-220">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-220">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="0d5d3-221">flags</span><span class="sxs-lookup"><span data-stu-id="0d5d3-221">flags</span></span>  
<span data-ttu-id="0d5d3-222">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-222">A list of flags; optional.</span></span> <span data-ttu-id="0d5d3-223">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-223">The valid flags are as follows:</span></span>

### <a name="return-value---sendmail"></a><span data-ttu-id="0d5d3-224">戻り値 - sendMail</span><span class="sxs-lookup"><span data-stu-id="0d5d3-224">Return Value - sendMail</span></span>

<span data-ttu-id="0d5d3-225">状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-225">The status \#SUCCESS\_SUCCESS or an error code from the \#MAPI macro.</span></span>

## <a name="method-status"></a><span data-ttu-id="0d5d3-226">メソッド status</span><span class="sxs-lookup"><span data-stu-id="0d5d3-226">Method status</span></span>

<span data-ttu-id="0d5d3-227">最後の Mapi 操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-227">Retrieves the status of the last Mapi operation.</span></span>

```xpp
public int status()
```

### <a name="return-value---status"></a><span data-ttu-id="0d5d3-228">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="0d5d3-228">Return Value - status</span></span>

<span data-ttu-id="0d5d3-229">最後の Mapi 操作のステータス コード。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-229">The status code of the last Mapi operation.</span></span>

### <a name="remarks---status"></a><span data-ttu-id="0d5d3-230">備考 - status</span><span class="sxs-lookup"><span data-stu-id="0d5d3-230">Remarks - status</span></span>

<span data-ttu-id="0d5d3-231">ステータス コードは \#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-231">The status codes can be found in the \#MAPI macro.</span></span>

## <a name="method-new"></a><span data-ttu-id="0d5d3-232">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0d5d3-232">Method new</span></span>

<span data-ttu-id="0d5d3-233">Mapi クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0d5d3-233">Initializes an instance of the Mapi class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="0d5d3-234">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="0d5d3-234">Method finalize</span></span>

```xpp
public void finalize()
```

