---
title: "Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 (2018 年 3 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 の新機能または変更された機能について説明します。 このバージョンは 2018 年 3 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: a765d51c-52d3-45c5-b578-63b5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform update 13, Platform update 14, Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 21eb5d6038f747e82420e724df07b8cbf242a5d6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-15-march-2018"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 (2018 年 3 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 の新機能または変更された機能について説明します。 このバージョンは 2018 年 3 月にリリースされ、ビルド番号は 7.0.4841 です。

> [!NOTE]
> このプラットフォームのリリースは累積されます。 プラットフォーム更新 13、プラットフォーム更新 14、プラットフォーム更新 15 からの新しい機能および変更された機能、およびそれ以前のすべての更新プログラムが含まれています。 

### <a name="announcing-the-dynamics-365-spring-18-release-notes"></a>Dynamics 365 2018 年春リリース ノートの発表
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか? 

[2018 年春リリース ノートをダウンロードします](http://download.microsoft.com/download/1/C/0/1C0A4DB7-9CE8-4D25-AC7F-65579E713BA8/ReleaseNotes_Dynamics365_03192018.pdf)。 計画に使用できる単一の PDF 内のすべての詳細を、端から端まで徹底的に捕捉しました。 

### <a name="platform-update-15-bug-fixes"></a>プラットフォーム アップデート 15 のバグ修正プログラム
プラットフォーム更新プログラム 15 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=869898) を参照してください。

## <a name="ability-to-color-grid-rows-without-overlayering-via-formdatasource-ondisplayoptioninitialize-event"></a>FormDataSource OnDisplayOptionInitialize イベントを介してオーバーレイすることなくグリッド行の色分けをする機能
オーバーレイすることなくグリッド行の色分けをする機能が、FormDataSource 上で OnDisplayOptionInitialize イベントを介して可能になりました。

## <a name="accessibility-support-for-controls-and-forms-developed-using-the-cloud-platform"></a>クラウド プラットフォームを使用して開発されたコントロールとフォームのユーザー補助サポート 

アクセス可能なソフトウェアを提供するに対する取り組みを再確認することにより、この更新プログラムは既に豊富なユーザー補助機能セットを増やすことに焦点を当てています。 これらの更新プログラムは、Microsoft のアクセシビリティ標準に準拠するために、グリッド、表、フォームなどの多くのプラットフォーム コンポーネントを改善します。 キーボードを使用したタスクの実行の詳細サポートには、スクリーン リーダー、ハイコントラスト テーマや完全なラベル サポート、およびクラウド プラットフォームを使用して作成されたアプリケーションとの豊富な統合があり、これにより障害のあるユーザーのための追加環境が提供されます。

## <a name="client-based-alerts"></a>クライアントに基づく警告 
クライアント ベースの警告機能を使用すると、Finance and Operations クライアントを離れずに警告ルールを定義できます。 請求書の支払いや顧客の住所変更など、ビジネス イベントに基づいて警告を定義できます。 特定の条件が満たされる場合、ユーザーに警告する通知が表示されます。 

Dynamics 365 for Finance and Operations の重大なイベントの通知システムは、警告によって形成されます。 警告を使用することで、作業日に追跡するイベントに関する情報を常に受け取ることができます。 また、独自のルール セットを簡単に設定して、延滞出荷、削除された注文、変更された価格、またはその他対応が必要なイベントに関する警告を受け取ることができます。

警告の詳細については、[警告の概要](alerts-overview.md) を参照してください。

## <a name="data-entity-behavior-with-configuration-keys"></a>コンフィギュレーション キーを持つデータ エンティティの動作
データ管理では、データ エンティティ、テーブル、およびフィールドで設定されている構成キーに従います。 これらのコンポーネントの階層構造のため、データ管理では、それ自体およびその親コンフィグレーション キーが使用可能になっている場合、階層内の子を使用することができます。 親コンフィギュレーション キーが無効の場合、どの子もインポートおよびエクスポートに使用できなくなります。 この動作の詳細については、[データ エンティティおよびコンフィギュレーション キー](../../dev-itpro/data-entities/config-key-entities.md)を参照してください。

## <a name="embed-powerapps"></a>PowerApps の埋め込み
開発者や非テクニカル ユーザーがコードを記述することなくカスタム ビジネス アプリを構築できるサービスである Microsoft PowerApps はサポートされています。 埋め込み PowerApp はページに追加できるだけでなく、編集、削除、または共有することができます。 また、Finance and Operations からのデータを活用する PowerApp を構築することができます。 詳細については、「[PowerApps の埋め込み](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)」を参照してください。 

## <a name="extension-and-overlayering-options-in-visual-studio"></a>Visual Studio の拡張子およびオーバーレイヤ オプション
今回のリリースでは、Visual Studio で拡張機能とオーバーレイ オプションを表示する方法を調整しました。 拡張オプションが最初に表示され、オーバーレイオ プションが「カスタマイズ」から「オーバーレイ」に変更され、より明示的になりました。
いつでも可能な場合は、拡張子を使用する必要があります。 

カスタマイズ オプションが推奨される使用順に表示されるようになりました。
1.  拡張機能を作成
2.  新しいプロジェクトに拡張機能を作成する
3.  オーバーレイヤー

## <a name="message-center-has-been-upgraded-to-the-new-action-center-with-improved-notification-visuals-and-capabilities"></a>メッセージ センターは、通知ビジュアルと機能が改良された新しいアクション センターにアップグレードされました
メッセージ センターは、新しいアクション センターにアップグレードされました。 ビジュアルが最新の通知インターフェイスを反映するために更新されただけではなく、新しいメッセージング API を使用してアクション センターに送信されるメッセージに、通知の保持を含む追加機能、メッセージに関連付けられた 1 つ以上のアクションを指定する機能、ユーザーのリストまたはロールのリストにメッセージを送信する機能が付属します。 メッセージ センターへルーティングされたすべての既存のメッセージはアクション センターへ自動的に表示されます。

## <a name="move-master-data-from-one-environment-to-another-using-the-excel-add-in"></a>Excel アドインを使用した別の環境へのマスター データの移動 
Dynamics 365 for Talent では、「はじめに」 Workbooks が提供され、ユーザーが Excel を使用して対話形式でデータを表示、編集、作成できます。 Excel アドインを使用するこれらのワークブックは、生産的な環境設定操作を実現します。
この拡張機能では、ある環境から Excel にデータを読み込み、環境アドレスを変更してから、そのデータを新しい環境に公開することにより、データをある環境から別の環境に移動することができます。

詳細については、「[環境データのコピー](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#copy-environment-data)」を参照してください。

## <a name="power-users-can-add-custom-fields-to-forms-without-developer-customization"></a>Power User は、開発者カスタマイズなしのフォームにカスタム フィールドを追加することができます。 
多くのアプリケーションのカスタマイズには、既存のテーブルへの 1 つまたは複数のフィールドの追加、およびそれらをアプリケーション フォームに含めることがあります。 ほとんどのカスタマイズは、フィールドを追加で構成される場合があります。

開発、テスト、およびコード ライフ サイクル管理のために開発者が操作する必要があるため、カスタマイズは高価です。 カスタマイズは、ある環境から別の環境にも管理および移行する必要があります。  

Dynamics 365 for Finance and Operations のフォームへのカスタム フィールドの追加を簡単にしました。 開発者向けのカスタマイズは不要になりました。 代わりに、パワー ユーザーはカスタム フィールドをテーブルに追加してから、個人用設定を使用してフォームにそのフィールドを配置できます。 IT 管理者は個人用設定を組織内で他のユーザーと共有できます。 カスタム フィールドを作成および管理する方法の詳細については、[カスタム フィールド](user-defined-fields.md) を参照してください。

## <a name="sr-10-certifications-for-dynamics-365-for-finance-and-operations"></a>(SR 10) Finance and Operations の Dynamics 365 の証明書 

**ISO 27001(Secure)** – ISO 27001 認証は、サービスが情報セキュリティ管理システム (ISMS) で概説されているコントロールおよび仕様に準拠していることを確認します。 ISO 27001 を達成することにより、お客様のビジネスを実行するために当社のサービスが安全であることが保証されます。 これを選択した場合は、ISO27001 認定サービスでビジネスを実行していることを監査人に安心させることで、自分のビジネスを証明するサポートにも役立ちます。

**ISO 27018 (個人データの保護)** – ISO 27018 は、クラウド内の個人情報の保護を対象としています。 Dynamics 365 for Finance and Operations は、ISO 27018 認証を取得しています。 マイクロソフトのサービスを使用して業務を管理するとき、個人の機密データはクラウドで安全かつ保護されることを理解していただくことを望みます。 また、業務に独自の ISO 27018 認証の取得を選択した場合、監査担当者は Finance and Operations に ISO 27108 認証があることを評価します。 

**SOC-1/Type-2 および SOC-2/Type-2** – サービス組織制御レポート (SOC) は、クラウド サービスに財務データが安全かつ保護されていることを保証するためのコントロールの設定があることを確認するのに役立ちます。 Finance and Operations は SOC-1/Type-2 および SOC-2/Type-2 認証を獲得しました。


## <a name="support-for-display-and-edit-methods-on-form-data-sources-using-augmentation-classes-extensionof"></a>拡張クラス (ExtensionOf) を使用したフォーム データ ソースの表示および編集メソッドのサポート

次の例では、テーブルやフォームの強化されたクラスの表示/編集メソッドを使用します。

#### <a name="class-extension-for-a-form"></a>フォームのクラスの拡張機能

```
[ExtensionOf(formstr(abForm))]
public final class abClassForm_Extension
{
    private Name previousName;
    private Counter noOfChanges;

    public display Name formExt_Display()
    {
        return previousName;
    }

    public edit Name formExt_Edit(boolean _set, Name _value)
    {
        if (_set)
        {
            noOfChanges++;
            previousName = strFmt("%1 %2", _value, noOfChanges);
        }

        return previousName;
    }
}
  ``` 
#### <a name="class-extension-for-a-table"></a>テーブルのクラスの拡張機能
  ``` 
[ExtensionOf(tablestr(abTable))]
public final class abClassTable_Extension
{
    public display Name tableExt_Display()
    {
        return "tableExt_Display " + this.FirstName + " " + this.LastName;
    }

    public edit Name tableExt_Edit(boolean _set, Name _value)
    {
        if (_set)
        {
            this.FirstName = "tableExt_Edit " +_value;
        }

        return this.FirstName;
    }
}
  ``` 
フォームまたはフォーム拡張は、DataMethod プロパティに `<ClassName>.<MethodName>` を指定することによって、フォーム コントロールから表示および編集メソッドを消費することができます。

