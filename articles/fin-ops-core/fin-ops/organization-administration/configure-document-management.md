---
title: ドキュメント管理のコンフィギュレーション
description: このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。
author: jasongre
ms.date: 06/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ffd926749d7b4e628e26dd03697a5090dfc1e8c389503e6ae146571963c3550
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768379"
---
# <a name="configure-document-management"></a>ドキュメント管理のコンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。 これには、この機能に関連する概念および機能に関する情報が含まれています。

ドキュメントの管理の詳細については、簡単なビデオ [ドキュメント管理](https://www.youtube.com/watch?v=p4rl1CkiLN4&feature=youtu.be) をご視聴ください。

## <a name="configure-document-types"></a>ドキュメント タイプのコンフィギュレーション

ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。 各ドキュメント タイプは、固有の場所に格納されることができます。

ドキュメント タイプの既定のセットが用意されています。 これらのドキュメント タイプを使用すると、ファイル、イメージ、メモ、または URL として添付ファイルを分類できます。 **ファイル** および **画像** の既定のドキュメント タイプは、場所として **Azure ストレージ** を使用するよう構成されます。

新しいドキュメント タイプを作成するには、次の手順に従います。

1. **ドキュメント タイプ** ページに移動します。
2. **新規** をクリックします。
3. **タイプ** フィールドに、**SharePoint** または **HR** ドキュメントなどの新しいドキュメント タイプの短縮名を入力します。
4. **名前** フィールドに、**SharePoint ファイル** または **HR ドキュメント** などの長い名前を入力します。
5. **クラス** フィールドで、ドキュメント タイプの動作を定義するクラスを指定します。

    - **ファイルの添付** - ユーザーはファイルを要求されます。
    - **URL の添付** - ユーザーは、`https://www.microsoft.com` のように、**メモ** フィールドに URL を入力することができます。 **添付ファイル** ページの **開く** ボタンをクリックすると [参照] タブに URL が開きます。
    - **簡易メモ** – ユーザーは **メモ** フィールドに簡易メモを追加できます。

6. **クラス** フィールドで **ファイルの添付** を指定した場合、**場所** フィールドで使用する記憶域メカニズムを指定します。
7. **場所** フィールドで **SharePoint** を指定した場合、**SharePoint アドレス** フィールドで Microsoft SharePoint アドレスを指定します。 これを行うには、**編集** ボタン (鉛筆シンボル) をクリックし、**フォルダー選択** ダイアログ ボックスをオンにします。

## <a name="configure-sharepoint-storage"></a>SharePoint 記憶域のコンフィギュレーション

Microsoft SharePoint Online は、ネイティブでサポートされる保存場所の 1 つです。 現在、SharePoint Online だけがサポートされています。 オンプレミス SharePoint (ローカル SharePoint サーバー) のサポートは将来追加される可能性があります。 

> [!IMPORTANT]
> SharePoint ストレージは、Microsoft が管理する環境でのみ使用可能です。

SharePoint ストレージを使用するには、ドキュメント タイプの **場所** フィールドを **SharePoint** に設定します。 その後、**SharePoint アドレス** フィールドに、有効な SharePoint アドレスを入力します。

SharePoint 記憶域を構成するには、次の手順を実行します。

1. **ドキュメント管理パラメータ** ページに移動します。
2. **SharePoint** タブの **既定の SharePoint サーバー** フィールドで、contosoax7.sharepoint.com など、SharePoint サイトに対して自動的に検出されたホスト名を確認します。 通常、SharePoint ホスト名は tenantname.sharepoint.com の形式で、そのテナントのアカウントは `user1@tenantname.onmicrosoft.com` の形式で示されます。

    既定の SharePoint サーバーが指定されていない場合は、通常、テナントの SharePoint サイトが存在しないか、有効な Microsoft 365 ライセンスが現在のユーザー (管理者) に関連付けられていないかのどちらかです。

4. オプション: **SharePoint 接続** のテスト をクリックし、指定された SharePoint ホスト名をテストします。 これでセキュリティとライセンスが正しく機能していることを確認します。 
5. オプション: **SharePoint を開く** をクリックし、指定された SharePoint ホスト名をブラウザーで開きます。 これはセキュリティを検証せず、ブラウザのタブで SharePoint パスを開くだけの簡単に検索であることに注意してください。

### <a name="troubleshooting-sharepoint-communication"></a>SharePoint 通信のトラブルシューティング

SharePoint 通信は、次の条件が満たされた場合にのみ、現在のユーザーに対して機能します。

- Microsoft 365 ライセンスが、ユーザーのアカウントに関連付けられています。
- ユーザーは、外部ユーザーではなくテナントの一般的なユーザーです (別のテナントのユーザーなど)。
- テナント用の SharePoint サイト (たとえば、 Contoso.SharePoint.com など) が存在します。
- SharePoint サイトでは、**このサイトが検索結果として表示されるのを許可** するように構成されています。
- ユーザーは、ドキュメントが格納されているフォルダにアクセスできます。

SharePoint に保存されているドキュメントが開かず、プレビューに表示されない場合は、次の手順に従って問題をトラブルシューティングします: 

1. 管理者アカウントに電子メール アカウントが関連付けられていることを確認します (**ユーザー** ページで確認または変更します)。 これが設定されていない場合は、OData Excel アドインを使用して電子メールとプロバイダーを追加する必要があります。 既定では、Excel デザインに電子メール アドレスは表示されません。 ユーザーは、Excel デザインを編集し、すべてのフィールドを追加し、適用、および更新する必要があります。 完了すると、管理者アカウントを更新できます。

2. 管理者アカウントに電子メール アカウントが関連付けられたら、Dynamics に管理者としてサインインします。

3. SharePoint に保存されている添付ファイルを開きます。

4. 添付ファイル ページおよび構成されている SharePoint フォルダーに対する読み取りアクセス権を持つ別のユーザー アカウントでログインします。 添付ファイルを開いてプレビューすることもできることを確認します。

## <a name="configure-file-types"></a>ファイルの種類のコンフィギュレーション

許可されているファイル拡張子のリストを変更することで、ユーザーがレコードに添付できるファイルの種類を制御できます。

ファイル タイプを指定するには、次の手順に従います。

1. **ドキュメント管理パラメータ** ページに移動します。
2. **ファイル タイプ** タブで、既定のファイル タイプを確認します。
3. ユーザーがレコードに添付できないファイル タイプを削除し、ユーザーがレコードに添付できるファイル タイプを追加します。

## <a name="configure-document-preview"></a>ドキュメント プレビューのコンフィギュレーション

添付ファイルのプレビューには、Microsoft Office Online Server で提供される Web アプリ オープン プラットフォーム インターフェイス (WOPI) を使用します。 **ドキュメント管理パラメーター** ページの **全般** タブの **Office Web Apps サーバー** フィールドで、添付ファイルのプレビューに使用する Office Online サーバー インスタンスを指定します。 既定値は、クラウドベースの WOPI サーバーをポイントする `https://onenote.officeapps.live.com` です。 

> [!NOTE]
> 次の場合は、指定通りの **Office Web Apps サーバー** フィールドを調整する必要があります。 
> -  中国の環境では、https://onenote.partner.officewebapps.cn を使用します。 
> -  Government Commmunity Cloud (GCC) の環境では、https://gb4-onenote.officeapps.live.com を使用します。

### <a name="for-a-microsoft-dynamics-365-finance--operations-on-premises-environment"></a>Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境の場合

財務 + 運営の規定のクラウドベース WOPI サーバーが、プレビューを提供する添付ファイルを読み込みできません。 プレビューが必要な場合は、[オンプレミス Office Online サーバー インスタンスをインストールし](/officeonlineserver/deploy-office-online-server)、それを環境内で構成する必要あります。 **Office Web アプリケーション サーバー** フィールドを、インストールされている Office Online Server インスタンスのホスト名に設定し、**保存** をクリックします。

プレビューが必要な場合は、**Office Web アプリケーション サーバー** フィールドを `https://localhost` に設定します。 プレビューは、その後は、エラー メッセージではなく、「プレビューを利用できません」というメッセージを表示します。

### <a name="document-preview-wopi-will-not-work-in-environments-with-an-ip-safe-list-enabled"></a>ドキュメント プレビュー (WOPI) は、IP セーフ リストが有効になっている環境では機能しません

プレビューを提供する WOPI サービスは、ファイル サービスに接続してファイルを取得してレンダリングすることができないため、ドキュメント プレビュー (WOPI) は、IP セーフ リストが有効になっている環境では動作しません。

## <a name="other-configuration"></a>他のコンフィギュレーション

これらのオプションが使用されることはほとんどありませんが、考慮すべきその他のコンフィギュレーション オプションを次に示します。

- **ドキュメント管理パラメーター** ページの、**一般** タブで、**ドキュメント テーブルの使用** オプションを使用して、**アクティブ ドキュメント テーブル** 許可リストを有効にすることができます。 このオプションを **はい** に設定すると、他のすべてのテーブルの添付ファイルが無効になります。 したがって、必要なときにのみこのオプションをオンにしてください。
- **ドキュメント管理パラメーター** ページの、**全般** タブで、**最大ファイル サイズ(単位: メガバイト)** フィールドを使用して、添付ファイルの最大ファイル サイズを設定できます。 SharePoint がドキュメント タイプとして使用される場合、ユーザーは最大ファイル サイズが 262 メガバイトのドキュメントのみをアップロードできます。 
- **オプション** ページ (**設定** \> **ユーザー オプション**) では、**基本設定** タブで、**ドキュメント処理の有効化** オプションを使用して、ドキュメント処理を無効にします (ドキュメント管理)。

## <a name="accessing-document-management-attachments"></a>ドキュメント管理添付ファイルへのアクセス 

ドキュメント管理は、データを含むほとんどのページのトップにある **添付** ボタンとして、ユーザーに表示されます。 **添付** ボタンを選択した場合 (または対応するキーボード ショートカット **Ctrl**+**Shift**+**A** を使用した場合)、ページで現在選択されているコントロールのデータ ソースのコンテキストで **添付ファイル** ページが開きます。 このページには、対応するデータ ソースに関連するすべての添付ファイルが表示されます。 

**添付** ボタンには、現在選択されているレコードの添付ファイルの数も表示されます。 したがって、現在のレコードの添付ファイルが存在するかどうかを確認するには、**添付ファイル** ページを開いておく必要はありません。 このボタンでは、0 ～ 9 件の添付ファイルの正確なカウントが表示されます。 9 つ以上の添付ファイルがある場合、このボタンには、**9+** がカウントとして表示されます。 このようにして、カウントが大きくなると生じる可能性があるパフォーマンスへの影響と視覚的なノイズが減少します。

### <a name="showing-related-document-attachments"></a>関連ドキュメントの添付ファイルの表示
バージョン 10.0.12 では、**関連するドキュメントの添付ファイルを表示** 機能により、ドキュメント添付ファイルのエクスペリエンスが次の方法で変更されます。 

-  この機能を有効にする場合、1 つのデータ ソースに関連する添付ファイルだけが **添付ファイル** ページに表示されなくなります。 代わりに、ユーザーは有効なレコードに関連付けられている、ページ上の他のデータ ソースから添付ファイルを表示してアクセスできます。 これを生じさせるため、データ ソースが次の条件を実行する必要があります。 
    -  内部結合または外部結合を使用して、親データソースに直接関連付けられます。
    -  基数が 1:1 または 0:1 のアクティブ、遅延、またはパッシブ結合を使用して、親データソースに直接関連付けられます。

    この基準では、ヘッダー レコードでの添付ファイルの表示時に、子コレクション (明細行など) からの添付ファイルの表示が除外されます。  

    **添付** ボタンの添付ファイルの数についても、この変更が反映されます。 

-  ユーザーは **添付ファイル** ページの関連するデータ ソース間で、添付ファイルを移動したりコピーしたりできます。

## <a name="document-attachment-history"></a>ドキュメントの添付ファイルの履歴

バージョン 10.0.16/プラットフォーム更新プログラム 40 以降、レコードの添付ファイルに対して履歴メカニズムが使用できます。 これにより、個々の添付ファイルに関連するアクションの監査を組織で管理することができます。 特に、添付ファイルが作成された日時、マークされた保留中の削除、復元、削除、または移動、そのアクションを実行したユーザーを表示できます。 添付ファイルの履歴は 10.0.16/プラットフォーム更新プログラム 40 まで維持されないため、そのバージョンよりも前の添付ファイルに対するアクションは使用できないことに注意してください。  

### <a name="configuration-of-document-attachment-history"></a>ドキュメントの添付ファイル履歴のコンフィグレーション
**ドキュメント管理パラメータ** > **一般** > **履歴** > **ドキュメント履歴の有効化** に移動してドキュメントの添付ファイルの履歴を有効 (または無効) にできます。 既定の履歴保持期間は 180 日ですが、この値は **履歴を保持する日数** フィールドを使用して必要に応じて変更できます。 

### <a name="viewing-an-attachments-history"></a>添付ファイルの履歴の表示
レコード添付ファイルの履歴を表示するには、2 つのエントリ ポイントがあります。

- 特定のレコードの添付ファイル確認するときは (詳細については [ドキュメント管理添付ファイルへのアクセス](configure-document-management.md#accessing-document-management-attachments) セクションを参照してください)、アクション ウィンドウの **ドキュメント履歴** ボタンを選択すると **添付ファイル** ページで現在の添付ファイル セットの履歴を表示できます。   
- 管理者は、**ドキュメント管理パラメータ** ページの **履歴** セクションで **ドキュメント履歴** ボタンを選択できます。 このアクションは、システム内のすべての添付ファイルの一覧を表示する **ドキュメント履歴** ページを開きます。 その後、任意のレコードをドリルダウンして選択した添付ファイルの詳細な履歴を確認します。  

## <a name="attachment-recovery"></a>添付ファイルの回復

プラットフォーム更新プログラム 29 では、添付ファイルの回復機能が追加され、設定された期間内に回復されるレコードの添付ファイルのごみ箱が提供されます。

### <a name="configuration-of-attachment-recovery"></a>添付ファイルの復元のコンフィギュレーション

**ドキュメント管理パラメータ** > **一般** >  **遅延削除** > **遅延削除の有効化** に移動して添付ファイルの回復を有効にできます。 **削除を延期する日数** のデフォルトは 30 日ですが、必要に応じて変更できます。 **削除を延期する日数** 値がゼロの場合、削除された添付ファイルが無期限に回復可能であることを意味します。 

添付ファイルの回復を有効にすると、この名前のバッチジョブが作成されます: "保存期間の終了に達した削除済み参照のスキャン"。 このバッチ ジョブは **削除を延期する日数** を使用して、**削除されたデータと時間** に基づいて削除された添付ファイルを保持する期間を決定します。

### <a name="deleting-attachments-when-attachment-recovery-is-active"></a>添付ファイルの回復がアクティブな場合の添付ファイルの削除

ユーザーが添付ファイルを削除すると通知がメッセージ センターに追加され、削除の確認と削除が意図されていない場合にアクションを取り消すオプションが提供されます。

テーブル拡張サポートが組み込まれているため、**DocuRef** や **DocuValue** テーブルの拡張やカスタム フィールド値は保持されリカバリが可能です。 

### <a name="recovering-attachments"></a>添付ファイルの回復

添付ファイルの回復が有効な場合、添付ファイルは次の 3 つの方法のいずれかで回復できます:
1. 削除した後すぐに、ユーザーは **添付ファイルを削除しました** 通知の [元に戻す] リンクを使用できます。
2. **添付ファイル** ページで **削除済み添付ファイル** ボタンを使用して、特定のレコードで回復できる削除された添付ファイルのリストにアクセスできます。 削除された添付ファイルは、確認のために開いたり、完全に削除したり、復元できます。
3. **システム管理** > **照会** で **削除済み添付ファイル** ページから削除された添付ファイルのリストへのアクセスが提供され、任意のレコードに回復できます。 削除された添付ファイルは、確認のために開いたり、完全に削除したり、復元できます。

## <a name="scanning-attachments-for-viruses-and-malicious-code"></a>添付ファイルでのウイルスおよび悪意のあるコードのスキャン
添付ファイルを操作するときに、ウイルスや悪意のあるコードを探すためのファイルをスキャンしたいかもしれません。 したがって、バージョン10.0.12 以降では、ユーザーが添付ファイルを操作するときに、選択したファイル スキャン ソフトウェアでファイル アップロード プロセスに統合できるように、拡張ポイントを使用できます。 ファイルのアップロードに同様の拡張点も利用可能です。 詳細については、[ファイルのアップロード コントロール](../../dev-itpro/user-interface/file-upload-control.md)を参照してください。

> [!IMPORTANT]
> 初期状態では、Finance and Operations アプリはファイルのウイルスや悪意のあるコードをスキャンせず、ファイルをスキャンするための特定のソフトウェアはお勧めしません。 代わりに、お客様は、独自のファイル スキャン ソフトウェアを選択し、ファイルのスキャンにソフトウェアまたはサービスを使用できるように適切なコードをデリゲート ハンドラーに追加する必要があります。

**Docu** クラスでは、次の 2 つのデリゲートが公開されます。 これらのデリゲートに対して、ドキュメントのスキャンを目的としてハンドラーを実装できます。

- **Docu.delegateScanDocument()** – このデリゲートによって、新しいドキュメント添付ファイルがアップロードされたときに、またはユーザーが既存の添付ファイルをプレビューまたはダウンロードしようとしたときに、ファイル スキャン ロジックが適用されます。 スキャン サービスによってファイルが悪質であると判断された場合、対応するアクションは失敗します。
-  **Docu.delegateScanDeletedDocument()**: このデリゲートによって、ユーザーがファイルをプレビューまたはダウンロードしようとしたときに、ファイルのスキャン ロジックが添付ファイルのごみ箱ドキュメントに適用されます。 スキャン サービスによってファイルが悪質であると判断された場合、対応するアクションは失敗します。

### <a name="implementation-details"></a>実装詳細
次の **ScanDocuments** クラスの例は、2 つのハンドラーの定型コードを示しています。 デリゲートのハンドラーを実装する方法の一般情報については、[要求または応答シナリオの EventHandlerResult クラス](../../dev-itpro/dev-tools/event-handler-result-class.md)を参照してください。

```xpp
    public final class ScanDocuments
    {

        [SubscribesTo(classStr(Docu), staticDelegateStr(Docu, delegateScanDocument))]
        public static void Docu_delegateScanDocument(DocuRef _docuRef, EventHandlerRejectResult _validationResult)
        {
            if (!ScanDocuments::scanDocument(_docuRef))
            {
                _validationResult.reject();
            }
        }

        [SubscribesTo(classStr(Docu), staticDelegateStr(Docu, delegateScanDeletedDocument))]
        public static void Docu_delegateScanDeletedDocument(DocuDeletedRef _docuDeletedRef, EventHandlerRejectResult _validationResult)
        {
            if (!ScanDocuments::scanDeletedDocument(_docuDeletedRef))
            {
                _validationResult.reject();
            }
        }

        private static boolean scanDocument(DocuRef _docuRef)
        {
            /*
            Custom implementation required for connecting to a scanning service
            If document scanning process found an issue, return false; otherwise, return true;
            */
            return true;
        }

        private static boolean scanDeletedDocument(DocuDeletedRef _docuDeletedRef)
        {
            /*
            Custom implementation required for connecting to a scanning service
            If document scanning process found an issue, return false; otherwise, return true;
            */
            return true;
        }

    }
```

## <a name="developer-specifying-valid-content-types-when-attaching-documents-programmatically"></a>[開発者] ドキュメントをプログラムで関連付ける際の有効なコンテンツのタイプを指定

`DocumentManagement` クラスからの次の API を使用すると、開発者は関連付けるファイルのファイル コンテンツ タイプ (MIME タイプ) を指定できます。 
-  attachFileToCommon()
-  attachFile()
-  attachFileToDocuRef()

このファイル コンテンツ タイプが正しく指定されていない場合、関連付けられているドキュメントが予期した動作をしない可能性があります。 このため、これらの API を使用する場合は、次のいずれかのアクション コースを考慮する必要があります。  

-  先行する API のいづれかで、`_fileContentType` パラメーターの **null** を渡します。 これにより、ファイル名から正しいコンテンツ タイプを推定できます。 
-  `_fileContentType` パラメータを含めない次のいずれかの方法で切り替えます。 これにより、誤ったファイル コンテンツ タイプを受け渡す可能性が回避されます。
    -  attachFileToCommon() を置き換える **attachFileForRecord()**
    -  attachFile() を置き換える **attachFileForReference()**
    -  attachFileToDocuRef() を置き換える **attachFileForDocuRefRecord()**

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="what-is-the-difference-between-document-handling-and-document-management"></a>ドキュメント処理とドキュメント管理の違いは何ですか。

ドキュメント処理とドキュメント管理の違いはありません。 両方とも同じ機能を示します。 異なるバージョンの製品では、異なる用語が使用されています。

### <a name="what-is-the-difference-between-document-management-and-print-management"></a>ドキュメント処理と印刷管理の違いは何ですか。

ドキュメント管理では、メモ、ドキュメント、および他のファイルを追加し記録できます。

印刷管理では選択したレポートの印刷設定を制御することができます。 印刷設定には、コピー数、印刷先、およびレポートに含めることができる多言語テキストが含まれます。 詳細については、 [ドキュメント レポーティング サービス](../../dev-itpro/analytics/document-reporting-services.md) を参照してください。

### <a name="what-is-the-difference-between-document-types-and-file-types"></a>ドキュメント タイプとファイル タイプの違いは何ですか。

ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。 各ドキュメント タイプは、固有の場所に格納されることができます。 ドキュメント タイプのテーブルの名前は DocuType です。

ファイル タイプには、Microsoft Word ドキュメントおよび画像が含まれます。 ファイル タイプは、.txt、.png、.doc、.xlsx、または .pdf などのファイルの拡張子で表されます。

### <a name="does-document-management-integrate-with-microsoft-365"></a>ドキュメント管理は Microsoft 365 と統合されますか?

はい。 SharePoint 記憶域はネイティブでサポートされ、ドキュメント タイプの保管場所として選択できます。 さらに、任意の URL アドレス指定可能なファイルを **URL** ドキュメント タイプ経由で添付できます。

### <a name="what-is-the-default-storage-location-for-attachments-in-finance--operations-environments"></a>Finance + Operations 環境での添付ファイルの既定の保管場所はどこですか?

既定では、添付ファイルは製品クラウド オファリングの一部として、自動的に Azure Blob 記憶域に保存されます。

### <a name="if-i-accidentally-delete-an-attachment-stored-in-azure-blob-storage-can-it-be-restored"></a>誤って Azure Blob Storage に格納されている添付ファイルを削除した場合、復元できますか。

Azure Blob Storage に格納されている添付ファイルが誤って削除された場合は、完全に削除されたことになり、ファイルへの参照情報も削除されてしまうため、復元や修復することができません。

### <a name="is-the-database-information-about-attachments-stored-separately-from-the-attachments-themselves"></a>添付ファイルに関するデータベースの情報は、添付ファイルそのものとは別の場所に保存されていますか？

添付ファイルの情報はDocuRefテーブルおよびDocuViewテーブルに格納されています。 DocuRefテーブルは、主に添付ファイルに関する情報を保持しています。 DocuRefの情報は、DocuViewレコードに関連付けられている情報と連携しています。 DocuRefテーブルは、添付ファイルを保持しています。 ファイルはデータベースの外に保存されるため、バックアップから復元するなどのデータベース上の操作は添付ファイルに関するデータベース情報のみに作用し、添付ファイルそのものには作用しません。

### <a name="can-attachments-be-stored-in-the-database"></a>添付ファイルをデータベースに保存できますか。

一連番号 既定では、添付ファイルは Azure Blob Storage に格納されます。

### <a name="what-are-the-main-differences-between-azure-blob-storage-and-database-storage"></a>Azure Blob Storage とデータベース ストレージの主な相違点は何ですか。

データベース ストレージは Azure SQL データベースです。 ファイル ストレージは Azure Blob Storage です。 Azure Blob Storage はよりシンプルで安価です。

### <a name="how-much-storage-do-we-get-for-azure-blob-storage"></a>Azure Blob Storage にどのくらいストレージを確保できますか。

詳細については [ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544) を参照してください。 現在、40 ギガバイト (GB) のストレージを使用できます。

### <a name="what-is-the-cost-for-additional-storage"></a>追加ストレージの費用はいくらですか。

追加ストレージのコストは変動しますが [標準の Azure ストレージ費用](https://azure.microsoft.com/pricing/details/storage/page-blobs/) と同様です。 すなわち、費用はおよそ GB あたり $0.05 です。

### <a name="how-can-we-learn-how-much-storage-weve-already-used"></a>既に使用しているストレージの量を確認する方法を教えてください。

データベースやファイル ストレージの制限に近づいた場合は、積極的なコミュニケーションが必要になります。 ただし、Microsoft Dynamics Lifecycle Services (LCS) は一部の情報を提供し、追加情報のサポート要求をログに記録できます。 

### <a name="is-there-an-option-to-export-all-document-attachments-from-the-system"></a>すべてのドキュメントの添付ファイルをシステムからエクスポートするか選択できますか。

添付ファイルをエクスポートできますが、標準の添付ファイル エンティティが存在しないため、その機能は標準の機能ではありません。 特定のビジネス ドキュメントやレコードに対する添付ファイルを提供するエンティティを作成する必要があります。

### <a name="how-can-attachments-be-extracted-from-the-system"></a>どのようにシステムから添付ファイルを抽出できますか。

添付ファイルを抽出するには、特定のビジネス ドキュメントやレコードに対する添付ファイル エンティティが作成される必要があります。 各レコード タイプの ID が異なるため、標準の添付ファイル エンティティがありません。 添付ファイル エンティティを作成する方法については、**AOT > データモデル > データ エンティティ** ノードの下にある "添付ファイル" を検索して、アプリケーション エクスプローラーの例を参照してください。

### <a name="how-does-the-document-preview-work-for-attachments-stored-in-sharepoint"></a>SharePoint に保存された添付ファイルにおけるドキュメント プレビューのしくみ。

ファイルは、WOPI サービスによって現在のユーザーのアクセス許可を使用して SharePoint から取得されます。 これらのファイルは、ドキュメント プレビューを表示するために HTML で表示されます。 つまり、現在のユーザーは、ファイルをプレビューしたり開いたりするためにファイルにアクセスできる必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
