<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="sysmailer-develop.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>sysmailer-develop.baf807.7826d799ba449a2261243d8191fd164998beb538.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>7826d799ba449a2261243d8191fd164998beb538</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\sysmailer-develop.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Develop email experiences by using the SysMailer framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysMailerフレームワークを使用して電子メール体験を開発する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how you can use the SysMailer framework to send email in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations で SysMailer フレームワークを使用して、電子メールを送信する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Develop email experiences by using the SysMailer framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysMailerフレームワークを使用して電子メール体験を開発する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Sending emails</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メールを送信しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The SysMailer framework is a new, extensible way to send email in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysMailer フレームワークは、Microsoft Dynamics 365 for Finance and Operations で電子メールを送信するための新しい拡張可能な方法です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It replaces all previous application programming interfaces (APIs) for mail, such as CDO.Messaging (SysMailer), MAPI (SysINetMail), and Outlook COM (SmmOutlookEmail).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CDO.Messaging (SysMailer), MAPI (SysINetMail), および Outlook COM (SmmOutlookEmail) などの電子メールに対して以前のすべてのアプリケーション プログラミング インターフェイス (API) が置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Those older mail APIs won't work correctly in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの古いメールの API は Finance and Operations で正しく動作しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>By taking advantage of the SysPlugin framework and several .NET technologies, SysMailer provides a configurable experience for users and enables the application consumers to remain agnostic to the email option that users use to send email.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysPlugin フレームワークと複数の .NET テクノロジを活用することで、SysMailer はユーザー向けのコンフィギュレーション可能な処理を提供し、アプリケーション使用者が電子メールを送信する際に使用する電子メール オプションに依存しない状態を維持することを可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The SysMailer framework consists of a factory class that is used to retrieve an email provider, a set of email providers that send messages, a message builder that builds the messages, and the forms that are related to configuring and interacting with the email providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysMailer フレームワークは電子メール プロバイダー、メッセージを送信する一連の電子メール プロバイダー、メッセージを構築するメッセージ ビルダー、およびコンフィギュレーションや電子メール プロバイダーとのやり取りに関連付けられているフォームを取得するために使用されるファクトリ クラスから構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To consume the SysMailer framework, an application developer primarily uses the <bpt id="p1">**</bpt>SysMailerFactory<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SysMailerMessageBuilder<ept id="p2">**</ept> classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysMailer フレームワークを使用するには、アプリケーション開発者は主に、<bpt id="p1">**</bpt>SysMailerFactory<ept id="p1">**</ept> クラスおよび <bpt id="p2">**</bpt>SysMailerMessageBuilder<ept id="p2">**</ept> クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The email provider factory is used to retrieve interactive or non-interactive email providers, so that multiple messages can be sent at the same time, or so that a message can be sent directly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール プロバイダ ファクトリを使用して、対話型または非対話型の電子メール プロバイダーを取得します。それにより複数のメッセージを同時に送信でき、または直接メッセージを送信できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The email providers expect the messages that they send to be encapsulated in .NET <bpt id="p1">**</bpt>System.Net.Mail.MailMessage<ept id="p1">**</ept> objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール プロバイダーはメッセージが .NET <bpt id="p1">**</bpt>System.Net.Mail.MailMessage<ept id="p1">**</ept> オブジェクトでカプセル化されることを予想して送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The message builder class is used to build the .NET object that is passed to the email provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージ ビルダ クラスは、電子メール プロバイダーに渡される .NET オブジェクトを構築するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This topic describes three scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、3 つのシナリオについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Sending an interactive message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対話型メッセージを送信しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Sending a non-interactive (batch) message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非対話型 (バッチ) メッセージを送信しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Sending multiple non-interactive (batch) messages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の非対話型 (バッチ) メッセージを送信しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Sending an interactive message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対話型メッセージを送信しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The following example is taken from the <bpt id="p1">**</bpt>CustCollectionsEmail<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は <bpt id="p1">**</bpt>CustCollectionsEmail<ept id="p1">**</ept> クラスから取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>It demonstrates multiple features of the framework, such as the ability to chain message builder calls, conditionally set the sender address ("from" address), and add attachments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージ ビルダーの呼び出しをつなぎ、条件付きで送信者のアドレス (「元」住所) を設定し、添付ファイルを追加する機能など、フレームワークの複数の機能を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Sending a non-interactive (batch) message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非対話型 (バッチ) メッセージを送信しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The following example is taken from the <bpt id="p1">**</bpt>VendRequestCompanyWorkflowManager<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は <bpt id="p1">**</bpt>VendRequestCompanyWorkflowManager<ept id="p1">**</ept> クラスから取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>It shows how you can send a single message non-interactively.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非対話型で単一のメッセージを送信する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Sending multiple non-interactive (batch) messages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の非対話型 (バッチ) メッセージを送信しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The following example is taken from the <bpt id="p1">**</bpt>UserAdAddManager<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は <bpt id="p1">**</bpt>UserAdAddManager<ept id="p1">**</ept> クラスから取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>It shows how you can get an instance of a batch email provider before you iterate over a list of emails to send.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信する電子メールの一覧を反復処理する前に、バッチ電子メール プロバイダーのインスタンスを取得する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Important considerations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な考慮事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>A sender address ("from" address) is required when messages are sent to an email provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">送信者のアドレス (「送信元」住所) は、電子メール プロバイダーにメッセージを送信する際に必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>A receiver address ("to" address) is required when messages are sent non-interactively.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">受取人のアドレス (「送付先」住所) は、メッセージが非対話型の際に必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>If these conditions aren't met, the framework throws an exception.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの条件を満たしていない場合、フレームワークは例外をスローします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If <bpt id="p1">**</bpt>getMessage<ept id="p1">**</ept> is called on the message builder before any call to <bpt id="p2">**</bpt>setFrom<ept id="p2">**</ept> is made, the builder tries to set the sender address to the current user's email address or network alias.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>setFrom<ept id="p2">**</ept> への呼び出しが行われる前にメッセージ ビルダーで <bpt id="p1">**</bpt>getMessage<ept id="p1">**</ept> が呼び出された場合、ビルダーは送信者のアドレスを、現在のユーザーの電子メール アドレスもしくはネットワーク エイリアスに設定しようとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When messages are sent, the way that the sender address ("from" address) is used depends on the provider:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが送信されるときに、送信者のアドレス (「元」住所) を使用する方法は、プロバイダーによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>EML provider:<ept id="p1">**</ept> The sender address is removed from the message before the message is opened in the user's email client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>電子メール プロバイダー:<ept id="p1">**</ept> ユーザーの電子メール クライアントでメッセージが開かれる前に、送信者のアドレスはメッセージから削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Therefore, the email client can set the sender address to the default account that is configured for sending mail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、電子メール クライアントは、送信者アドレスを、メールの送信用に構成された既定のアカウントに設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>SMTP provider:<ept id="p1">**</ept> The Simple Mail Transfer Protocol (SMTP) server must be configured to allow messages to be sent by using the sender address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SMTP プロバイダー:<ept id="p1">**</ept>Simple Mail Transfer Protocol (SMTP) サーバーは、送信者のアドレスを使用してメッセージを送信できるように構成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In other words, the SMTP server must allow the impersonation of emails that are sent from it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、SMTP サーバーはそこから送信される電子メールの偽装ができるようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Otherwise, the SMTP server might prevent the messages from being sent, flag them as spam, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合は、SMTP サーバーはメッセージの送信、スパムとしてのフラグ付けなどを防ぐ可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>When messages are sent, the framework returns a Boolean value that indicates whether the operation to send the message was successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが送信されると、フレームワークはメッセージを送信する操作が成功したかどうかを示すブール値を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>However, it doesn't report any messages to the Action Center when the operation is successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、操作が成功した場合には、アクション センターにメッセージはレポートされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>You decide whether messages are shown in the Action Center.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション センターにメッセージが表示されるかどうかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>By default, the body of all messages that are sent is in rich-text (HTML) format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、すべてのメッセージの本文はリッチ テキスト (HTML) 形式で送信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>If an application scenario requires that plain text be used to maintain newline spacing, you can pass <bpt id="p1">**</bpt>false<ept id="p1">**</ept> to the optional <bpt id="p2">**</bpt><ph id="ph1">\_</ph>isHtml<ept id="p2">**</ept> parameter of the <bpt id="p3">**</bpt>setBody<ept id="p3">**</ept> method on the message builder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションのシナリオで、改行の間隔を維持するためにテキスト形式を使用する必要がある場合、<bpt id="p1">**</bpt>false<ept id="p1">**</ept> をメッセージ ビルダーの <bpt id="p3">**</bpt>setBody<ept id="p3">**</ept> メソッドのオプションの <bpt id="p2">**</bpt><ph id="ph1">\_</ph>isHtml<ept id="p2">**</ept> パラメーターに渡すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Adding a new email provider</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい電子メール プロバイダーを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You can add email providers by using the pluggable framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグが可能なフレームワークを使用して電子メール プロバイダーを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>When you use the factory class and interfaces, new email providers immediately become available for use across all relevant application scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出荷時のクラスとインターフェイスを使用すると、新しい電子メールプロバイダは、関連するすべてのアプリケーション シナリオですぐに使用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Examples of email providers can be found in the existing provider implementations, SysMailerEML and SysMailerSMTP, and also in an existing tutorial implementation, Tutorial<ph id="ph1">\_</ph>SysMailerMailTo.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール プロバイダーの例は、既存のプロバイダーの実装 SysMailerEML および SysMailerSMTP、または既存のチュートリアルの実装 Tutorial<ph id="ph1">\_</ph>SysMailerMailTo を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The examples that follow are excerpts from the implementation of the SysMailerEML email provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、SysMailerEML 電子メール プロバイダーの実装からの抜粋です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To implement an email provider, you must create an implementation class that has the following properties:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール プロバイダーを実装するには、以下のプロパティを持つ実装クラスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The class must have the appropriate <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスには、適切な<bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept>の属性が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The class must implement the base <bpt id="p1">**</bpt>SysIMailer<ept id="p1">**</ept> methods, <bpt id="p2">**</bpt>getId<ept id="p2">**</ept> and <bpt id="p3">**</bpt>getDescription<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスでは、基準の <bpt id="p1">**</bpt>SysIMailer<ept id="p1">**</ept> メソッド、<bpt id="p2">**</bpt>getId<ept id="p2">**</ept> および <bpt id="p3">**</bpt>getDescription<ept id="p3">**</ept> を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The class must implement the <bpt id="p1">**</bpt>SysImailerInteractive<ept id="p1">**</ept> interface, the <bpt id="p2">**</bpt>SysIMailerNonInteractive<ept id="p2">**</ept> interface, or both interfaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスでは <bpt id="p1">**</bpt>SysImailerInteractive<ept id="p1">**</ept> インターフェイス、<bpt id="p2">**</bpt>SysIMailerNonInteractive<ept id="p2">**</ept> インターフェイス、または両方のインターフェイスを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Specify attributes for the implementation class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装クラスの属性を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The first step is to specify attributes for the implementation class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の手順で実装クラスの属性を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The class must have two attributes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスには、2 つの属性が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>ExportAttribute<ept id="p1">**</ept> – The framework uses this attribute to discover the plug-in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExportAttribute<ept id="p1">**</ept> – フレームワークでは、この属性を使用してプラグインを検出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The attribute specifies that the plug-in is an implementation of <bpt id="p1">**</bpt>SysIMailer<ept id="p1">**</ept> and therefore part of the SysMailer framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性は、プラグインが <bpt id="p1">**</bpt>SysIMailer<ept id="p1">**</ept> の実装であるため SysMailer フレームワークの一部であることを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>ExportMetadataAttribute<ept id="p1">**</ept> – The framework uses this attribute to find specific instances of a plug-in that have specific metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExportMetadataAttribute<ept id="p1">**</ept> – フレームワークでは、この属性を使用して、特定のメタデータを持つプラグインの特定のインスタンスを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The attribute specifies the ID of the email provider, so that a single provider can be discovered quickly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性は、単一のプロバイダーをすばやく検出できるように電子メール プロバイダーの ID を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>No two email providers should ever have the same ID.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>2 つの電子メール プロバイダーは、同じ ID を持つ必要はありません。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Implement the SysIMailer interface</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysIMailer インターフェイスの実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The <bpt id="p1">**</bpt>SysIMailer<ept id="p1">**</ept> interface includes identifiable information about an email provider, regardless of the capabilities of the email provider itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysIMailer<ept id="p1">**</ept> インターフェイスには、電子メール プロバイダー自体の機能に関係なく、電子メール プロバイダーについて特定できる情報が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>To implement this interface, you must create two methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このインターフェイスを実行するには、2 つのメソッドを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>getId<ept id="p1">**</ept> – This method returns the same ID that is specified in the <bpt id="p2">**</bpt>ExportMetadataAttribute<ept id="p2">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>getId<ept id="p1">**</ept> – このメソッドは、<bpt id="p2">**</bpt>ExportMetadataAttribute<ept id="p2">**</ept> 属性で指定される 同じ ID を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>getDescription<ept id="p1">**</ept> – This method returns a non-technical description that indicates how the email will be sent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>getDescription<ept id="p1">**</ept> – このメソッドは、どのように電子メールを送信するかを示す非技術的な記述を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Implement a combination of the SysIMailerInteractive and SysIMailerNonInteractive interfaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysIMailerInteractive および SysIMailerNonInteractive インターフェイスの組み合わせを実装します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The <bpt id="p1">**</bpt>SysIMailerInteractive<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SysIMailerNonInteractive<ept id="p2">**</ept> interfaces are very simple.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysIMailerInteractive<ept id="p1">**</ept> および <bpt id="p2">**</bpt>SysIMailerNonInteractive<ept id="p2">**</ept> インターフェイスは非常に簡単です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>They implement the <bpt id="p1">**</bpt>sendInteractive<ept id="p1">**</ept> and <bpt id="p2">**</bpt>sendNonInteractive<ept id="p2">**</ept> methods, respectively.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは <bpt id="p1">**</bpt>sendInteractive<ept id="p1">**</ept> および <bpt id="p2">**</bpt>sendNonInteractive<ept id="p2">**</ept> メソッド、をそれぞれ実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>An email provider might implement one or both methods, depending on its capabilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール プロバイダーは、その機能に応じて、一方または両方の方法を実装できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Each method that is implemented takes a .NET <bpt id="p1">**</bpt>System.Net.Mail.MailMessage<ept id="p1">**</ept> object that you use to construct and send the email.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装されている各メソッドは、電子メールの作成と送信に使用する .NET <bpt id="p1">**</bpt>System.Net.Mail.MailMessage<ept id="p1">**</ept> オブジェクトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The <bpt id="p1">**</bpt>System.Net.Mail.MailMessage<ept id="p1">**</ept> object contains a large amount of advanced functionality that is related to MIME messages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>System.Net.Mail.MailMessage<ept id="p1">**</ept> オブジェクトには、MIME メッセージに関連する高度な機能が多数含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You can build a relatively complex message object and pass it to an email provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">比較的複雑なメッセージ オブジェクトを作成して、電子メール プロバイダーに渡すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>If there is specific functionality that an email provider doesn't support, the email provider is expected to handle the functionality actively (by modifying the message), passively (by making an internal call to another email provider), or not at all (by throwing an error).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール プロバイダーがサポートしていない特定の機能がある場合、電子メール プロバイダーは機能を能動的に (メッセージを変更して) 処理するか、受動的に (別の電子メール プロバイダーを内部的に呼び出して) 処理するか、またはまったく (エラーをスローして) 処理しないことが予想されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Migration from Microsoft Dynamics AX 2012 to Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 から Finance and Operations への移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Migration involves using the <bpt id="p1">**</bpt>SysMailerMessageBuilder<ept id="p1">**</ept> object to build a message and then using the <bpt id="p2">**</bpt>SysMailerFactory<ept id="p2">**</ept> to send it, as outlined in the examples in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移行には、このトピックの例に示すように <bpt id="p1">**</bpt>SysMailerMessageBuilder<ept id="p1">**</ept> オブジェクトを使用して メッセージを構築し、<bpt id="p2">**</bpt>SysMailerFactory<ept id="p2">**</ept> を使用して送信することが含まれます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>