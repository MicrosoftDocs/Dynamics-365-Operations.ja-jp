---
title: Microsoft Dynamics 365 Commerce での Store Commerce アプリ (プレビュー)
description: このトピックでは、Store Commerce アプリの設定および構成方法について説明します。
author: mugunthanm
ms.date: 08/23/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-20-2020
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: a73e0528904e03e5c8473680ee215abe07c862ea
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414598"
---
# <a name="store-commerce-app-in-microsoft-dynamics-365-commerce-preview"></a>Microsoft Dynamics 365 Commerce での Store Commerce アプリ (プレビュー)

[!include [banner](../includes/banner.md)]



このトピックは、Microsoft Dynamics 365 Commerce バージョン 10.0.20 およびそれ以降に適用されます。

Store Commerce アプリケーションは、Modern Point of Sale (MPOS) および Cloud POS (CPOS) を 1 つのアプリケーションに統合し、拡張機能を含めて MPOS および CPOS の機能を保持しながら、小売業者に配置の選択肢を提供し、パフォーマンスの向上や、優れたアプリケーションライフ サイクル管理を行う、現物店舗向けの次世代オファリングです。

Dynamics 365 Commerce の Store Commerce アプリは、レジ担当者、販売担当者、販売在庫担当者、在庫担当者、および店舗管理者などの第一線の作業者に豊富なコマース機能を提供します。 これらの作業者は、現金売りトランザクション、現金/シフト管理、顧客契約、支援販売、クライアンテリング、エンドレス アイル、注文処理/フルフィルメント、在庫管理、レポートなどのコマース操作を実行することができます。

Store Commerce は、MPOSとCPOSの両方の利点を提供します。

> [!NOTE]
> Store Commerceは、プレビュー アプリケーションとしてリリースされます。 同じくプレビュー中の [Microsoft Edge WebView2](/microsoft-edge/webview2/) コントロールが使用されます。 したがって、一般に使用可能になるまで実稼働環境で Store Commerce を使用 **しません**。

Store Commerce は、[Microsoft Edge WebView2](/microsoft-edge/webview2/) コントロールを使用してクラウド販売時点管理 (CPOS) アプリを表示する Windows 用のシェル アプリです。 CPOS は Web ブラウザーでのみ実行できますが、Store Commerce は [Modern 販売時点管理 (MPOS)](retail-modern-pos-architecture.md) などのネイティブ WIndows アプリとして実行できます。

Store Commerce はローカル ハードウェア ステーションをサポートし、支払ターミナル、プリンター、キャッシュ ドロワーに直接統合できます。 ハードウェア デバイスを使用するために共有のハードウェア ステーションを設定する必要はありません。

ユーザー インターフェイス (UI) を表示するために、Store Commerce は、ユニバーサル Windows プラットフォーム (UTC) アプリ表示フレームワークの代わりに Chromium エンジンを使用します。 Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。 MPOS と Store Commerce の主な違いは、Store Commerce がアプリを表示するのに Chromium エンジンを使用する点です。

## <a name="benefits-of-store-commerce"></a>Store Commerce の利点

+ Microsoft Store を使用した、簡略化したアプリケーション ライフサイクル管理 (ALM)。
+ MPOS または CPOS 用に開発された拡張機能または ISV コードは、Store Commerce で再利用できます。
+ Store Commerce は、MPOSとCPOSの両方の利点を提供します。
+ パフォーマンス向上。
+ POS および拡張機能のアップグレードがより簡単になりました。
+ 専用のハードウェア ステーション (HWS) をサポートしています。
+ 将来オフラインでサポートされます。

## <a name="application-lifecycle-management"></a>アプリケーション ライフサイクル管理

Store Commerce は、Windows デバイスで実行するアプリです。 [Windows アプリ- Microsoft Store](https://aka.ms/StoreCommerceApp) から入手できるので、検索、ダウンロード、および配置が容易になります。 したがって、配置とサービスの全体的なライフサイクルは簡素化されます。

Store Commerce には、上位互換性と下位互換性の両方があります。 このアプリは、Windows ポリシーを設定するか、Intune のような Microsoft Store のアプリでサポートされている更新プログラムや配置ツールを使用して簡単に更新できます。 このアプリは、Cloud Scale Unit (CSU) および拡張機能とは別に更新できます。

MPOS の場合は、アプリを取得して拡張機能にパッケージ化するために、手動の管理が必要です。 ただし、Store Commerce は Microsoft Store を通じて配置されるので、アプリケーション ライフサイクル管理 (ALM) を大幅に簡素化できます。

Store Commerce は、CPOS を表示するシェルです。 したがって、更新された CPOS 機能を取得するには、CPOS も更新する必要があります。 CPOS は CSU から更新できます。 CSU の更新方法の詳細については、[Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md) を参照してください。

![Store Commerce。](media/StoreCommerce.PNG)


## <a name="store-commerce-and-mpos-parity"></a>Store Commerce と MPOS の機能

Store Commerce は、将来 MPOS と同等の機能を持つようになります。 現時点では、Store Commerce はオフラインでの実行をサポートしません (Headless Commerce への接続がない場合)。 さまざまな POS アプリおよびトポロジの詳細については [Modern POS (MPOS) かクラウド POS かの選択](../mpos-or-cpos.md) を参照する

## <a name="store-commerce-and-cpos-parity"></a>Store Commerce と CPOS の機能

Store Commerce では CPOS が表示され、CPOS と同等の機能を持つほか、Store Commerce は専用のハードウェア ステーションをサポートし、将来はオフラインでサポートすることができます。

## <a name="choosing-between-store-commerce-and-mposcpos"></a>Store Commerce か MPOS/CPOS かの選択

現在、MPOS または CPOS を使用している場合、Store Commerce に移動することができます。 現在、Store Commerce アプリケーションはプレビュー中です。つまり、このアプリはテスト環境または UAT 環境で試す必要があります。

Store Commerce では CPOS が表示されますが、MPOS と同等の機能があります。 Store Commerce と MPOS はユニバーサル Windows プラットフォーム (UTC) アプリで、ローカル ハードウェア ステーションをサポートしています。 Store Commerce は現在、オフラインでサポートされていませんが、将来サポートされる予定です。 

Store Commerceでは、UI を表示するために Chromium エンジンが使用され、表示パフォーマンスが MPOS よりも向上します。 さらに、Store Commerce は Microsoft Store を通じて配置されるので、ALM を大幅に簡素化できます。 対照的に、MPOS は Microsoft Dynamics Lifecycle Service (LCS) と Commerce 本社を使用してセルフサービスを行います。

店舗でオフライン サポートの必要がない場合、パフォーマンスの向上やより容易なライフサイクル管理などの、付加的なメリットのため、MPOS の代わりに Store Commerce を選択する必要があります。

<table>
<thead>
<tr>
<th></th>
<th>Store Commerce (プレビュー)</th>
<th>MPOS</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row">操作環境</th>
<td>Windows</td>
<td>Windows</td>
</tr>
<tr>
<th scope="row">ALM</th>
<td>Store Commerce は Microsoft Store を通じて配置され、CPOS は CSU を通じて配置します。</td>
<td>MPOS は、LCS および Commerce 本社を使用してセルフサービスを行います。 MPOS インストーラーを使用してパッケージ化され、インストールされます。</td>
</tr>
<tr>
<th scope="row">拡張子</th>
<td>拡張機能は CPOS に配置します。</td>
<td>拡張機能が MPOS と共にパッケージ化されるか、あるいは独立した拡張パッケージが使用されます。</td>
</tr>
<tr>
<th scope="row">オフライン モードでのサポート</th>
<td>いいえ (将来追加する予定)</td>
<td>あり</td>
</tr>
<tr>
<th scope="row">ローカル ハードウェア ステーションのサポート</th>
<td>あり</td>
<td>あり</td>
</tr>
<tr>
<th scope="row">UI レンダリング エンジン</th>
<td>UI の表示には、Curomium エンジンが使用されます。</td>
<td>UI の表示には UWP アプリの表示フレームワークが使用されます。</td>
</tr>
</tbody>
</table>

## <a name="setup-and-installation"></a>設定およびインストール

### <a name="prerequisite"></a>前提条件

+ Windows 10 バージョン 17763.0 またはそれ以上、または Windows Server 2019。
+ Microsoft Edge、アプリは Microsoft Edge WebView2 コントロールを使用するためです。
+ Dynamics 365 Commerce (バック オフィスおよび CPOS)。

### <a name="device-setup-in-commerce-headquarters"></a>Commerce 本社でのデバイスの設定

Store Commerce のために、**Store Commerce** という名前の新しいアプリケーション タイプが **デバイス** ページに追加されました (**Retail と Commerce \> チャネル設定 \> POS 設定 \> デバイス**)。 Store Commerce でデバイスを作成する場合、このアプリケーション タイプを選択します。

Store Commerce アプリケーション タイプがドロップ ダウン メニューで表示されない場合は、Retail と Commerce > 本社設定 > パラメーター > コマース パラメーター > 一般 > **初期化子** から **初期化** 実行し、ページを更新します。

Store Commerce のために[登録](../tasks/create-associate-registers.md) と[デバイス](../tasks/create-associate-device.md) を作成する必要があります。 その後、アプリを有効にする前に、Commerce 本社の配送スケジュールからレジスター ジョブを実行します。 デバイスの作成中に、**アプリケーション タイプ** フィールドを **Store Commerce** に設定します。

Store Commerce は Microsoft Store で使用できます。 アプリをダウンロードおよびインストールするには、これらの手順に従います。

1. [Windows アプリ- Microsoft Store](https://aka.ms/StoreCommerceApp) を開き、**Store Commerce** を検索します。
2. **入手** を選択し、アプリをインストールします。 
3. Windows の **スタート** メニューで **Store Commerce** を検索し、アプリを開きます。

アプリの起動後、次の手順に従って、アプリを構成および有効化します。

1. アプリの開始ページに、CPOS の URL を入力します。 このURLは、LCSの環境詳細ページ、または Commerce の **チャネル プロファイル** ページで確認できます (**Dynamics 365 Commerce\> チャネル設定 \> チャネル プロファイル**)。
2. **保存** を選択します。
3. Store Commerce を有効にするには、POS有効化ガイドの [POS の有効ガイド](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation) の手順に従います。
4. 従業員アカウントを使用してサイン インします。

これで、コマース操作を完了できます。

### <a name="troubleshooting-setup-issues"></a> 設定の問題に関するトラブルシューティング

#### <a name="reset-the-app"></a>アプリのリセット

入力した CPOS URL が無効で、変更したい場合、または、有効化の際にアプリがエラー状態にある場合は、アプリをリセットしてプロセスを再開できます。

1. Windowsvの **スタート** メニューで、アプリを選択したまま (あるいは右クリックして) 、それから **詳細 \>アプリの設定** を選択します。
2. アプリ設定ページを **リセット** ボタンが見つかるまで下にスクロールします。
3. **リセット** を選択し、表示されたらアプリのリセットを確認します。

## <a name="customizing-the-app"></a>アプリのカスタマイズ

Retail ソフトウェア開発キット (SDK) が提供する POS 拡張機能サポートを使用して、Store Commerce をカスタマイズできます。 POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更、検証の追加、カスタム機能の追加を行うことができます。 - 詳細については、[販売時点管理 (POS) の拡張機能の概要](pos-extension/pos-extension-overview.md) を参照してください。

Retail SDK を使用して開発された拡張機能は、CPOS、MPOS、および Store Commerce で機能します。 ただし、MPOS と CPOSによって拡張機能をパッケージ化して配置する方法は異なります。

Store Commerce では CPOS が表示されるので、CPOS のパッケージと配置のオプションに従って Store Commerce の拡張機能を配置する必要があります。

### <a name="hardware-station-extension"></a>ハードウェア ステーション拡張機能

Store Commerceは、ハードウェア デバイスと統合できるよう拡張することができます。 GitHub で追加された[サンプル拡張機能コード](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample) を使用して、Store Commerce ハードウェア ステーションの拡張機能 (HWS) のパッケージを生成できます。 詳細については [POS と新しいハードウェア デバイスの統合](hardware-device-extension.md) を参照してください。

## <a name="known-issues-with-the-microsoft-edge-webview2-control"></a>Microsoft Edge WebView2 コントロールに関する既知の問題

+ 有効化の際に、複数のオプションを使用して AAD パスワードを入力するように求めるメッセージが表示されたら、パスワードを選択します。 他のオプションが機能しない場合があります。
+ Tab キーを押すと、アプリ内のタブが機能しない場合があります。 代わりに、項目をクリックまたは選択します。
+ マウスを使用してドロップダウンを選択できない場合があります。 代わりに、キーボードを使用して選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
