---
title: SysMailerフレームワークを使用して電子メール体験を開発する
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations で SysMailer フレームワークを使用して、電子メールを送信する方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 05/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 270774
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: d13f17257b904bedee7415276c0808de3638c1b3
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537259"
---
# <a name="develop-email-experiences-by-using-the-sysmailer-framework"></a><span data-ttu-id="9e995-103">SysMailerフレームワークを使用して電子メール体験を開発する</span><span class="sxs-lookup"><span data-stu-id="9e995-103">Develop email experiences by using the SysMailer framework</span></span>

[!include [banner](../includes/banner.md)]

## <a name="sending-emails"></a><span data-ttu-id="9e995-104">電子メールを送信しています</span><span class="sxs-lookup"><span data-stu-id="9e995-104">Sending emails</span></span>

<span data-ttu-id="9e995-105">SysMailer フレームワークは、Microsoft Dynamics 365 for Finance and Operations で電子メールを送信するための新しい拡張可能な方法です。</span><span class="sxs-lookup"><span data-stu-id="9e995-105">The SysMailer framework is a new, extensible way to send email in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9e995-106">CDO.Messaging (SysMailer), MAPI (SysINetMail), および Outlook COM (SmmOutlookEmail) などの電子メールに対して以前のすべてのアプリケーション プログラミング インターフェイス (API) が置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="9e995-106">It replaces all previous application programming interfaces (APIs) for mail, such as CDO.Messaging (SysMailer), MAPI (SysINetMail), and Outlook COM (SmmOutlookEmail).</span></span> <span data-ttu-id="9e995-107">これらの古いメールの API は Finance and Operations で正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="9e995-107">Those older mail APIs won't work correctly in Finance and Operations.</span></span> <span data-ttu-id="9e995-108">SysPlugin フレームワークと複数の .NET テクノロジを活用することで、SysMailer はユーザー向けのコンフィギュレーション可能な処理を提供し、アプリケーション使用者が電子メールを送信する際に使用する電子メール オプションに依存しない状態を維持することを可能にします。</span><span class="sxs-lookup"><span data-stu-id="9e995-108">By taking advantage of the SysPlugin framework and several .NET technologies, SysMailer provides a configurable experience for users and enables the application consumers to remain agnostic to the email option that users use to send email.</span></span>

<span data-ttu-id="9e995-109">SysMailer フレームワークは電子メール プロバイダー、メッセージを送信する一連の電子メール プロバイダー、メッセージを構築するメッセージ ビルダー、およびコンフィギュレーションや電子メール プロバイダーとのやり取りに関連付けられているフォームを取得するために使用されるファクトリ クラスから構成されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-109">The SysMailer framework consists of a factory class that is used to retrieve an email provider, a set of email providers that send messages, a message builder that builds the messages, and the forms that are related to configuring and interacting with the email providers.</span></span> <span data-ttu-id="9e995-110">SysMailer フレームワークを使用するには、アプリケーション開発者は主に、**SysMailerFactory** クラスおよび **SysMailerMessageBuilder** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="9e995-110">To consume the SysMailer framework, an application developer primarily uses the **SysMailerFactory** and **SysMailerMessageBuilder** classes.</span></span> <span data-ttu-id="9e995-111">電子メール プロバイダ ファクトリを使用して、対話型または非対話型の電子メール プロバイダーを取得します。それにより複数のメッセージを同時に送信でき、または直接メッセージを送信できます。</span><span class="sxs-lookup"><span data-stu-id="9e995-111">The email provider factory is used to retrieve interactive or non-interactive email providers, so that multiple messages can be sent at the same time, or so that a message can be sent directly.</span></span> <span data-ttu-id="9e995-112">電子メール プロバイダーはメッセージが .NET **System.Net.Mail.MailMessage** オブジェクトでカプセル化されることを予想して送信します。</span><span class="sxs-lookup"><span data-stu-id="9e995-112">The email providers expect the messages that they send to be encapsulated in .NET **System.Net.Mail.MailMessage** objects.</span></span> <span data-ttu-id="9e995-113">メッセージ ビルダ クラスは、電子メール プロバイダーに渡される .NET オブジェクトを構築するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-113">The message builder class is used to build the .NET object that is passed to the email provider.</span></span>

### <a name="scenarios"></a><span data-ttu-id="9e995-114">シナリオ</span><span class="sxs-lookup"><span data-stu-id="9e995-114">Scenarios</span></span>

<span data-ttu-id="9e995-115">このトピックでは、3 つのシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9e995-115">This topic describes three scenarios:</span></span>

- <span data-ttu-id="9e995-116">対話型メッセージを送信しています</span><span class="sxs-lookup"><span data-stu-id="9e995-116">Sending an interactive message</span></span>
- <span data-ttu-id="9e995-117">非対話型 (バッチ) メッセージを送信しています</span><span class="sxs-lookup"><span data-stu-id="9e995-117">Sending a non-interactive (batch) message</span></span>
- <span data-ttu-id="9e995-118">複数の非対話型 (バッチ) メッセージを送信しています</span><span class="sxs-lookup"><span data-stu-id="9e995-118">Sending multiple non-interactive (batch) messages</span></span>

#### <a name="sending-an-interactive-message"></a><span data-ttu-id="9e995-119">対話型メッセージを送信しています</span><span class="sxs-lookup"><span data-stu-id="9e995-119">Sending an interactive message</span></span>

<span data-ttu-id="9e995-120">次の例は **CustCollectionsEmail** クラスから取得されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-120">The following example is taken from the **CustCollectionsEmail** class.</span></span> <span data-ttu-id="9e995-121">メッセージ ビルダーの呼び出しをつなぎ、条件付きで送信者のアドレス (「元」住所) を設定し、添付ファイルを追加する機能など、フレームワークの複数の機能を示します。</span><span class="sxs-lookup"><span data-stu-id="9e995-121">It demonstrates multiple features of the framework, such as the ability to chain message builder calls, conditionally set the sender address ("from" address), and add attachments.</span></span>

```
using (System.IO.Stream attachmentStream = this.generateAttachment())
{
    var messageBuilder = new SysMailerMessageBuilder();
    messageBuilder.addTo(context.parmEmailAddress())
    .setSubject(emailSubject)
    .setBody(SysEmailMessage::stringExpand(emailBody,
    SysEmailTable::htmlEncodeParameters(templateTokens)));
    if (emailSenderAddr)
    {
        messageBuilder.setFrom(emailSenderAddr, emailSenderName);
    }
    else if (custParameters.CollectionsOMTeam)
    {
        var collectionsEmail = OMTeam::find(custParameters.CollectionsOMTeam).primaryEmail();
        if (strLen(collectionsEmail) > 0)
        {
            messageBuilder.setFrom(collectionsEmail);
        }
    }
    if (attachmentStream != null)
    {
        messageBuilder.addAttachment(
            attachmentStream,
            strFmt('%1%2', strReplace(DateTimeUtil::toStr(DateTimeUtil::utcNow()), ':', ''), '.xlsx'));
    }
    SysMailerFactory::sendInteractive(messageBuilder.getMessage());
}
```

#### <a name="sending-a-non-interactive-batch-message"></a><span data-ttu-id="9e995-122">非対話型 (バッチ) メッセージを送信しています</span><span class="sxs-lookup"><span data-stu-id="9e995-122">Sending a non-interactive (batch) message</span></span>

<span data-ttu-id="9e995-123">次の例は **VendRequestCompanyWorkflowManager** クラスから取得されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-123">The following example is taken from the **VendRequestCompanyWorkflowManager** class.</span></span> <span data-ttu-id="9e995-124">非対話型で単一のメッセージを送信する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9e995-124">It shows how you can send a single message non-interactively.</span></span>

```
// The vendor <vendor name> has been approved and has been added to the vendor master.
messageText = strFmt("@SYS134393", DirPartyTable::findRec(vendRequestCompany.VendParty).Name);
// Request
var messageBuilder = new SysMailerMessageBuilder();
messageBuilder.setFrom(senderEmail)
    .addTo(recipientEmail)
    .setSubject("@SYS130372")
    .setBody(messageText);
SysMailerFactory::sendNonInteractive(messageBuilder.getMessage());
```

#### <a name="sending-multiple-non-interactive-batch-messages"></a><span data-ttu-id="9e995-125">複数の非対話型 (バッチ) メッセージを送信しています</span><span class="sxs-lookup"><span data-stu-id="9e995-125">Sending multiple non-interactive (batch) messages</span></span>

<span data-ttu-id="9e995-126">次の例は **UserAdAddManager** クラスから取得されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-126">The following example is taken from the **UserAdAddManager** class.</span></span> <span data-ttu-id="9e995-127">送信する電子メールの一覧を反復処理する前に、バッチ電子メール プロバイダーのインスタンスを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9e995-127">It shows how you can get an instance of a batch email provider before you iterate over a list of emails to send.</span></span>

```
var mail = SysMailerFactory::getNonInteractiveMailer();
var messageBuilder = new SysMailerMessageBuilder();
for (i = 1; i <= conLen(_notifyCon); i++)
{
    notifyEmailsStr = conPeek(_notifyCon, i);
    select firstonly RecId, Email from sysUser where sysUser.Id == notifyEmailsStr;
    if (sysUser.RecId && sysUser.Email != '')
    {
        messageBuilder.reset()
            .setFrom(_emailFrom)
            .addTo(sysUser.Email)
            .setSubject("@SYS129183")
            .setBody(errorStr);
        mail.sendNonInteractive(messageBuilder.getMessage());
        delete_from tmpUserErrorNotification;
    }
}
```

### <a name="important-considerations"></a><span data-ttu-id="9e995-128">重要な考慮事項</span><span class="sxs-lookup"><span data-stu-id="9e995-128">Important considerations</span></span>

- <span data-ttu-id="9e995-129">送信者のアドレス (「送信元」住所) は、電子メール プロバイダーにメッセージを送信する際に必要です。</span><span class="sxs-lookup"><span data-stu-id="9e995-129">A sender address ("from" address) is required when messages are sent to an email provider.</span></span> <span data-ttu-id="9e995-130">受取人のアドレス (「送付先」住所) は、メッセージが非対話型の際に必要です。</span><span class="sxs-lookup"><span data-stu-id="9e995-130">A receiver address ("to" address) is required when messages are sent non-interactively.</span></span> <span data-ttu-id="9e995-131">これらの条件を満たしていない場合、フレームワークは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="9e995-131">If these conditions aren't met, the framework throws an exception.</span></span> <span data-ttu-id="9e995-132">**setFrom** への呼び出しが行われる前にメッセージ ビルダーで **getMessage** が呼び出された場合、ビルダーは送信者のアドレスを、現在のユーザーの電子メール アドレスもしくはネットワーク エイリアスに設定しようとします。</span><span class="sxs-lookup"><span data-stu-id="9e995-132">If **getMessage** is called on the message builder before any call to **setFrom** is made, the builder tries to set the sender address to the current user's email address or network alias.</span></span>
- <span data-ttu-id="9e995-133">メッセージが送信されるときに、送信者のアドレス (「元」住所) を使用する方法は、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9e995-133">When messages are sent, the way that the sender address ("from" address) is used depends on the provider:</span></span>

    - <span data-ttu-id="9e995-134">**電子メール プロバイダー:** ユーザーの電子メール クライアントでメッセージが開かれる前に、送信者のアドレスはメッセージから削除されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-134">**EML provider:** The sender address is removed from the message before the message is opened in the user's email client.</span></span> <span data-ttu-id="9e995-135">したがって、電子メール クライアントは、送信者アドレスを、メールの送信用に構成された既定のアカウントに設定できます。</span><span class="sxs-lookup"><span data-stu-id="9e995-135">Therefore, the email client can set the sender address to the default account that is configured for sending mail.</span></span>
    - <span data-ttu-id="9e995-136">**SMTP プロバイダー:** Simple Mail Transfer Protocol (SMTP) サーバーは、送信者のアドレスを使用してメッセージを送信できるように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e995-136">**SMTP provider:** The Simple Mail Transfer Protocol (SMTP) server must be configured to allow messages to be sent by using the sender address.</span></span> <span data-ttu-id="9e995-137">つまり、SMTP サーバーはそこから送信される電子メールの偽装ができるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e995-137">In other words, the SMTP server must allow the impersonation of emails that are sent from it.</span></span> <span data-ttu-id="9e995-138">それ以外の場合は、SMTP サーバーはメッセージの送信、スパムとしてのフラグ付けなどを防ぐ可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9e995-138">Otherwise, the SMTP server might prevent the messages from being sent, flag them as spam, and so on.</span></span>

- <span data-ttu-id="9e995-139">メッセージが送信されると、フレームワークはメッセージを送信する操作が成功したかどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="9e995-139">When messages are sent, the framework returns a Boolean value that indicates whether the operation to send the message was successful.</span></span> <span data-ttu-id="9e995-140">ただし、操作が成功した場合には、アクション センターにメッセージはレポートされません。</span><span class="sxs-lookup"><span data-stu-id="9e995-140">However, it doesn't report any messages to the Action Center when the operation is successful.</span></span> <span data-ttu-id="9e995-141">アクション センターにメッセージが表示されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9e995-141">You decide whether messages are shown in the Action Center.</span></span>
- <span data-ttu-id="9e995-142">既定では、すべてのメッセージの本文はリッチ テキスト (HTML) 形式で送信されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-142">By default, the body of all messages that are sent is in rich-text (HTML) format.</span></span> <span data-ttu-id="9e995-143">アプリケーションのシナリオで、改行の間隔を維持するためにテキスト形式を使用する必要がある場合、**false** をメッセージ ビルダーの **setBody** メソッドのオプションの **\_isHtml** パラメーターに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="9e995-143">If an application scenario requires that plain text be used to maintain newline spacing, you can pass **false** to the optional **\_isHtml** parameter of the **setBody** method on the message builder.</span></span>

## <a name="adding-a-new-email-provider"></a><span data-ttu-id="9e995-144">新しい電子メール プロバイダーを追加</span><span class="sxs-lookup"><span data-stu-id="9e995-144">Adding a new email provider</span></span>

<span data-ttu-id="9e995-145">プラグが可能なフレームワークを使用して電子メール プロバイダーを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="9e995-145">You can add email providers by using the pluggable framework.</span></span> <span data-ttu-id="9e995-146">出荷時のクラスとインターフェイスを使用すると、新しい電子メールプロバイダは、関連するすべてのアプリケーション シナリオですぐに使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9e995-146">When you use the factory class and interfaces, new email providers immediately become available for use across all relevant application scenarios.</span></span> <span data-ttu-id="9e995-147">電子メール プロバイダーの例は、既存のプロバイダーの実装 SysMailerEML および SysMailerSMTP、または既存のチュートリアルの実装 Tutorial\_SysMailerMailTo を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e995-147">Examples of email providers can be found in the existing provider implementations, SysMailerEML and SysMailerSMTP, and also in an existing tutorial implementation, Tutorial\_SysMailerMailTo.</span></span> <span data-ttu-id="9e995-148">次の例は、SysMailerEML 電子メール プロバイダーの実装からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="9e995-148">The examples that follow are excerpts from the implementation of the SysMailerEML email provider.</span></span>

<span data-ttu-id="9e995-149">電子メール プロバイダーを実装するには、以下のプロパティを持つ実装クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e995-149">To implement an email provider, you must create an implementation class that has the following properties:</span></span>

- <span data-ttu-id="9e995-150">クラスには、適切な**エクスポート**の属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="9e995-150">The class must have the appropriate **Export** attributes.</span></span>
- <span data-ttu-id="9e995-151">クラスでは、基準の **SysIMailer** メソッド、**getId** および **getDescription** を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e995-151">The class must implement the base **SysIMailer** methods, **getId** and **getDescription**.</span></span>
- <span data-ttu-id="9e995-152">クラスでは **SysImailerInteractive** インターフェイス、**SysIMailerNonInteractive** インターフェイス、または両方のインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e995-152">The class must implement the **SysImailerInteractive** interface, the **SysIMailerNonInteractive** interface, or both interfaces.</span></span>

### <a name="specify-attributes-for-the-implementation-class"></a><span data-ttu-id="9e995-153">実装クラスの属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e995-153">Specify attributes for the implementation class</span></span>

<span data-ttu-id="9e995-154">最初の手順で実装クラスの属性を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e995-154">The first step is to specify attributes for the implementation class.</span></span> <span data-ttu-id="9e995-155">クラスには、2 つの属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="9e995-155">The class must have two attributes:</span></span>

- <span data-ttu-id="9e995-156">**ExportAttribute** – フレームワークでは、この属性を使用してプラグインを検出します。</span><span class="sxs-lookup"><span data-stu-id="9e995-156">**ExportAttribute** – The framework uses this attribute to discover the plug-in.</span></span> <span data-ttu-id="9e995-157">属性は、プラグインが **SysIMailer** の実装であるため SysMailer フレームワークの一部であることを指定します。</span><span class="sxs-lookup"><span data-stu-id="9e995-157">The attribute specifies that the plug-in is an implementation of **SysIMailer** and therefore part of the SysMailer framework.</span></span>
- <span data-ttu-id="9e995-158">**ExportMetadataAttribute** – フレームワークでは、この属性を使用して、特定のメタデータを持つプラグインの特定のインスタンスを検索します。</span><span class="sxs-lookup"><span data-stu-id="9e995-158">**ExportMetadataAttribute** – The framework uses this attribute to find specific instances of a plug-in that have specific metadata.</span></span> <span data-ttu-id="9e995-159">属性は、単一のプロバイダーをすばやく検出できるように電子メール プロバイダーの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e995-159">The attribute specifies the ID of the email provider, so that a single provider can be discovered quickly.</span></span> <span data-ttu-id="9e995-160">**2 つの電子メール プロバイダーは、同じ ID を持つ必要はありません。**</span><span class="sxs-lookup"><span data-stu-id="9e995-160">**No two email providers should ever have the same ID.**</span></span>

```
using System.IO;
using System.Net.Mail;
using System.Text.RegularExpressions;
#define.SysMailerEML_ID('EML')
/// <summary>
/// The <c>SysMailerEML</c> class is an interactive email provider implementation that sends messages by generating
/// an EML file, uploading it to Azure temporary blob storage, and then redirecting the user's browser to
/// the file to save or open for sending using their default email client.
/// </summary>
// This is a framework class. Customizing this class may cause problems with future upgrades to the software.
[System.ComponentModel.Composition.ExportAttribute(identifierStr(Dynamics.AX.Application.SysIMailer)),
System.ComponentModel.Composition.ExportMetadataAttribute(extendedTypeStr(SysMailerId), #SysMailerEML_ID)]
public class SysMailerEML implements SysIMailerInteractive
{
```

### <a name="implement-the-sysimailer-interface"></a><span data-ttu-id="9e995-161">SysIMailer インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="9e995-161">Implement the SysIMailer interface</span></span>

<span data-ttu-id="9e995-162">**SysIMailer** インターフェイスには、電子メール プロバイダー自体の機能に関係なく、電子メール プロバイダーについて特定できる情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e995-162">The **SysIMailer** interface includes identifiable information about an email provider, regardless of the capabilities of the email provider itself.</span></span> <span data-ttu-id="9e995-163">このインターフェイスを実行するには、2 つのメソッドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e995-163">To implement this interface, you must create two methods:</span></span>

- <span data-ttu-id="9e995-164">**getId** – このメソッドは、**ExportMetadataAttribute** 属性で指定される 同じ ID を返します。</span><span class="sxs-lookup"><span data-stu-id="9e995-164">**getId** – This method returns the same ID that is specified in the **ExportMetadataAttribute** attribute.</span></span>
- <span data-ttu-id="9e995-165">**getDescription** – このメソッドは、どのように電子メールを送信するかを示す非技術的な記述を返します。</span><span class="sxs-lookup"><span data-stu-id="9e995-165">**getDescription** – This method returns a non-technical description that indicates how the email will be sent.</span></span>

```
public SysMailerId getId()
{
    return #SysMailerEML_ID;
}
public SysMailerDescription getDescription()
{
    // Use an email app, such as Outlook
    return "@ApplicationFoundation:EmailProviderEMLDescription";
}
```

### <a name="implement-a-combination-of-the-sysimailerinteractive-and-sysimailernoninteractive-interfaces"></a><span data-ttu-id="9e995-166">SysIMailerInteractive および SysIMailerNonInteractive インターフェイスの組み合わせを実装します</span><span class="sxs-lookup"><span data-stu-id="9e995-166">Implement a combination of the SysIMailerInteractive and SysIMailerNonInteractive interfaces</span></span>

<span data-ttu-id="9e995-167">**SysIMailerInteractive** および **SysIMailerNonInteractive** インターフェイスは非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="9e995-167">The **SysIMailerInteractive** and **SysIMailerNonInteractive** interfaces are very simple.</span></span> <span data-ttu-id="9e995-168">これらは **sendInteractive** および **sendNonInteractive** メソッド、をそれぞれ実装します。</span><span class="sxs-lookup"><span data-stu-id="9e995-168">They implement the **sendInteractive** and **sendNonInteractive** methods, respectively.</span></span> <span data-ttu-id="9e995-169">電子メール プロバイダーは、その機能に応じて、一方または両方の方法を実装できます。</span><span class="sxs-lookup"><span data-stu-id="9e995-169">An email provider might implement one or both methods, depending on its capabilities.</span></span> <span data-ttu-id="9e995-170">実装されている各メソッドは、電子メールの作成と送信に使用する .NET **System.Net.Mail.MailMessage** オブジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e995-170">Each method that is implemented takes a .NET **System.Net.Mail.MailMessage** object that you use to construct and send the email.</span></span>

```
public boolean sendInteractive(System.Net.Mail.MailMessage _message)
{
    using (var emlStream = this.generateEmlFile(_message))
    {
        Dynamics.AX.Application.File::SendFileToUser(emlStream, 'message.eml');
    }
    return true;
}
```

<span data-ttu-id="9e995-171">**System.Net.Mail.MailMessage** オブジェクトには、MIME メッセージに関連する高度な機能が多数含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e995-171">The **System.Net.Mail.MailMessage** object contains a large amount of advanced functionality that is related to MIME messages.</span></span> <span data-ttu-id="9e995-172">比較的複雑なメッセージ オブジェクトを作成して、電子メール プロバイダーに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="9e995-172">You can build a relatively complex message object and pass it to an email provider.</span></span> <span data-ttu-id="9e995-173">電子メール プロバイダーがサポートしていない特定の機能がある場合、電子メール プロバイダーは機能を能動的に (メッセージを変更して) 処理するか、受動的に (別の電子メール プロバイダーを内部的に呼び出して) 処理するか、またはまったく (エラーをスローして) 処理しないことが予想されます。</span><span class="sxs-lookup"><span data-stu-id="9e995-173">If there is specific functionality that an email provider doesn't support, the email provider is expected to handle the functionality actively (by modifying the message), passively (by making an internal call to another email provider), or not at all (by throwing an error).</span></span>

## <a name="migration-from-microsoft-dynamics-ax-2012-to-finance-and-operations"></a><span data-ttu-id="9e995-174">Microsoft Dynamics AX 2012 から Finance and Operations への移行</span><span class="sxs-lookup"><span data-stu-id="9e995-174">Migration from Microsoft Dynamics AX 2012 to Finance and Operations</span></span>

<span data-ttu-id="9e995-175">移行には、このトピックの例に示すように **SysMailerMessageBuilder** オブジェクトを使用して メッセージを構築し、**SysMailerFactory** を使用して送信することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e995-175">Migration involves using the **SysMailerMessageBuilder** object to build a message and then using the **SysMailerFactory** to send it, as outlined in the examples in this topic.</span></span>
