---
title: SysMailerフレームワークを使用して電子メール体験を開発する
description: このトピックでは、SysMailer フレームワークを使用して、電子メールを送信する方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 05/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 270774
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 9a3c5e08cb9515b85c205efa1dc5d97247c4ec98
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183339"
---
# <a name="develop-email-experiences-by-using-the-sysmailer-framework"></a>SysMailerフレームワークを使用して電子メール体験を開発する

[!include [banner](../includes/banner.md)]

## <a name="sending-emails"></a>電子メールを送信しています

SysMailer フレームワークは、電子メールを送信するための新しい拡張可能な方法です。 CDO.Messaging (SysMailer), MAPI (SysINetMail), および Outlook COM (SmmOutlookEmail) などの電子メールに対して以前のすべてのアプリケーション プログラミング インターフェイス (API) が置き換えられます。 これらの古いメールの API は Finance and Operations アプリケーションで正しく動作しません。 SysPlugin フレームワークと複数の .NET テクノロジを活用することで、SysMailer はユーザー向けのコンフィギュレーション可能な処理を提供し、アプリケーション使用者が電子メールを送信する際に使用する電子メール オプションに依存しない状態を維持することを可能にします。

SysMailer フレームワークは電子メール プロバイダー、メッセージを送信する一連の電子メール プロバイダー、メッセージを構築するメッセージ ビルダー、およびコンフィギュレーションや電子メール プロバイダーとのやり取りに関連付けられているフォームを取得するために使用されるファクトリ クラスから構成されます。 SysMailer フレームワークを使用するには、アプリケーション開発者は主に、**SysMailerFactory** クラスおよび **SysMailerMessageBuilder** クラスを使用します。 電子メール プロバイダ ファクトリを使用して、対話型または非対話型の電子メール プロバイダーを取得します。それにより複数のメッセージを同時に送信でき、または直接メッセージを送信できます。 電子メール プロバイダーはメッセージが .NET **System.Net.Mail.MailMessage** オブジェクトでカプセル化されることを予想して送信します。 メッセージ ビルダ クラスは、電子メール プロバイダーに渡される .NET オブジェクトを構築するために使用されます。

### <a name="scenarios"></a>シナリオ

このトピックでは、3 つのシナリオについて説明します。

- 対話型メッセージを送信しています
- 非対話型 (バッチ) メッセージを送信しています
- 複数の非対話型 (バッチ) メッセージを送信しています

#### <a name="sending-an-interactive-message"></a>対話型メッセージを送信しています

次の例は **CustCollectionsEmail** クラスから取得されます。 メッセージ ビルダーの呼び出しをつなぎ、条件付きで送信者のアドレス (「元」住所) を設定し、添付ファイルを追加する機能など、フレームワークの複数の機能を示します。

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

#### <a name="sending-a-non-interactive-batch-message"></a>非対話型 (バッチ) メッセージを送信しています

次の例は **VendRequestCompanyWorkflowManager** クラスから取得されます。 非対話型で単一のメッセージを送信する方法を示します。

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

#### <a name="sending-multiple-non-interactive-batch-messages"></a>複数の非対話型 (バッチ) メッセージを送信しています

次の例は **UserAdAddManager** クラスから取得されます。 送信する電子メールの一覧を反復処理する前に、バッチ電子メール プロバイダーのインスタンスを取得する方法を示します。

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

### <a name="important-considerations"></a>重要な考慮事項

- 送信者のアドレス (「送信元」住所) は、電子メール プロバイダーにメッセージを送信する際に必要です。 受取人のアドレス (「送付先」住所) は、メッセージが非対話型の際に必要です。 これらの条件を満たしていない場合、フレームワークは例外をスローします。 **setFrom** への呼び出しが行われる前にメッセージ ビルダーで **getMessage** が呼び出された場合、ビルダーは送信者のアドレスを、現在のユーザーの電子メール アドレスもしくはネットワーク エイリアスに設定しようとします。
- メッセージが送信されるときに、送信者のアドレス (「元」住所) を使用する方法は、プロバイダーによって異なります。

    - **電子メール プロバイダー:** ユーザーの電子メール クライアントでメッセージが開かれる前に、送信者のアドレスはメッセージから削除されます。 したがって、電子メール クライアントは、送信者アドレスを、メールの送信用に構成された既定のアカウントに設定できます。
    - **SMTP プロバイダー:** Simple Mail Transfer Protocol (SMTP) サーバーは、送信者のアドレスを使用してメッセージを送信できるように構成する必要があります。 つまり、SMTP サーバーはそこから送信される電子メールの偽装ができるようにする必要があります。 それ以外の場合は、SMTP サーバーはメッセージの送信、スパムとしてのフラグ付けなどを防ぐ可能性があります。

- メッセージが送信されると、フレームワークはメッセージを送信する操作が成功したかどうかを示すブール値を返します。 ただし、操作が成功した場合には、アクション センターにメッセージはレポートされません。 アクション センターにメッセージが表示されるかどうかを決定します。
- 既定では、すべてのメッセージの本文はリッチ テキスト (HTML) 形式で送信されます。 アプリケーションのシナリオで、改行の間隔を維持するためにテキスト形式を使用する必要がある場合、**false** をメッセージ ビルダーの **setBody** メソッドのオプションの **\_isHtml** パラメーターに渡すことができます。

## <a name="adding-a-new-email-provider"></a>新しい電子メール プロバイダーを追加

プラグが可能なフレームワークを使用して電子メール プロバイダーを追加することができます。 出荷時のクラスとインターフェイスを使用すると、新しい電子メールプロバイダは、関連するすべてのアプリケーション シナリオですぐに使用できるようになります。 電子メール プロバイダーの例は、既存のプロバイダーの実装 SysMailerEML および SysMailerSMTP、または既存のチュートリアルの実装 Tutorial\_SysMailerMailTo を参照してください。 次の例は、SysMailerEML 電子メール プロバイダーの実装からの抜粋です。

電子メール プロバイダーを実装するには、以下のプロパティを持つ実装クラスを作成する必要があります。

- クラスには、適切な**エクスポート**の属性が必要です。
- クラスでは、基準の **SysIMailer** メソッド、**getId** および **getDescription** を実装する必要があります。
- クラスでは **SysImailerInteractive** インターフェイス、**SysIMailerNonInteractive** インターフェイス、または両方のインターフェイスを実装する必要があります。

### <a name="specify-attributes-for-the-implementation-class"></a>実装クラスの属性を指定します。

最初の手順で実装クラスの属性を指定します。 クラスには、2 つの属性が必要です。

- **ExportAttribute** – フレームワークでは、この属性を使用してプラグインを検出します。 属性は、プラグインが **SysIMailer** の実装であるため SysMailer フレームワークの一部であることを指定します。
- **ExportMetadataAttribute** – フレームワークでは、この属性を使用して、特定のメタデータを持つプラグインの特定のインスタンスを検索します。 属性は、単一のプロバイダーをすばやく検出できるように電子メール プロバイダーの ID を指定します。 **2 つの電子メール プロバイダーは、同じ ID を持つ必要はありません。**

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

### <a name="implement-the-sysimailer-interface"></a>SysIMailer インターフェイスの実装

**SysIMailer** インターフェイスには、電子メール プロバイダー自体の機能に関係なく、電子メール プロバイダーについて特定できる情報が含まれます。 このインターフェイスを実行するには、2 つのメソッドを作成する必要があります。

- **getId** – このメソッドは、**ExportMetadataAttribute** 属性で指定される 同じ ID を返します。
- **getDescription** – このメソッドは、どのように電子メールを送信するかを示す非技術的な記述を返します。

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

### <a name="implement-a-combination-of-the-sysimailerinteractive-and-sysimailernoninteractive-interfaces"></a>SysIMailerInteractive および SysIMailerNonInteractive インターフェイスの組み合わせを実装します

**SysIMailerInteractive** および **SysIMailerNonInteractive** インターフェイスは非常に簡単です。 これらは **sendInteractive** および **sendNonInteractive** メソッド、をそれぞれ実装します。 電子メール プロバイダーは、その機能に応じて、一方または両方の方法を実装できます。 実装されている各メソッドは、電子メールの作成と送信に使用する .NET **System.Net.Mail.MailMessage** オブジェクトを選択します。

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

**System.Net.Mail.MailMessage** オブジェクトには、MIME メッセージに関連する高度な機能が多数含まれます。 比較的複雑なメッセージ オブジェクトを作成して、電子メール プロバイダーに渡すことができます。 電子メール プロバイダーがサポートしていない特定の機能がある場合、電子メール プロバイダーは機能を能動的に (メッセージを変更して) 処理するか、受動的に (別の電子メール プロバイダーを内部的に呼び出して) 処理するか、またはまったく (エラーをスローして) 処理しないことが予想されます。

## <a name="migration-from-microsoft-dynamics-ax-2012-to-finance-and-operations-applications"></a>Microsoft Dynamics AX 2012 から Finance and Operations アプリケーションへの移行

移行には、このトピックの例に示すように **SysMailerMessageBuilder** オブジェクトを使用して メッセージを構築し、**SysMailerFactory** を使用して送信することが含まれます。
