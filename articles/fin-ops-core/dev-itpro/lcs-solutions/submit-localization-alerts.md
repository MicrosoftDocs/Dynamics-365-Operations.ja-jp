---
title: 国または地域固有の規制機能に関わる通知を送信
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) を使用して、ローカライズおよび Translation service を通じて警告を送信する方法について説明します。
author: kfend
ms.date: 12/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27791
ms.assetid: b37140b4-5d6f-460f-ae36-f0d7bd90c0d3
ms.openlocfilehash: 4d8e12d41004a3b0cc3ea0a1ac0de22b2c830977
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270731"
---
# <a name="submit-alerts-about-countryregion-specific-regulatory-features"></a>国または地域固有の規制機能に関わる通知を送信

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 規制警告送信サービスを通じて警告を送信する方法について説明します。 この記事は、計画およびリリースされた規制機能を、LCS 問題検索を使用して追跡する方法についても説明します。 

## <a name="accessing-the-regulatory-alert-submission-service"></a>規制の警告の送信サービスへのアクセス

Dynamics Lifecycle Services (LCS) において自身のまたは招待されたプロジェクトで規制警告送信サービスにアクセスするには、次のいずれかの操作を実行します。
- メニュー項目から **警告サービス** を選択します。
- ページの右側にスクロールし、**その他のツール** で **警告サービス** を選択します。 

**Dynamics 規制の警告の送信** ページが表示されます。 このページを使用すると、個人または組織が以前に提出したすべての警告を表示できます。

## <a name="submitting-a-regulatory-alert"></a>規制の警告の送信
新しい規制アラートを入力するには、**Dynamics 規制アラートの送信** ページの上部にあるプラス記号 (**+**) をクリックします。 **送信を警告** ウィザードが起動します。 このウィザードでは次のタスクを完了することができます。

- 既存の規制項目を検索します。
- 警告の説明をします。
- 送信を確認します。

### <a name="search-for-existing-regulatory-items"></a>既存の規制項目を検索

問題検索を使用して、警告に関連する規制機能が既に存在するかどうかを識別します。

1.  キーワード、国/地域、 Microsoft Knowledge Base (KB) 番号または Application Object Tree (AOT) オブジェクトなどの検索用語を入力します。 検索ボタンをクリックします。 製品問題または規制機能のいずれかに、検索用語を含むすべての項目が検索結果に表示されます。 使用可能なフィルターを使用して、検索を絞ることができます。
2.  ユーザーが探している規制における機能がない場合は、ブラウザー ウィンドウの下部にある **規制に関する警告を送信** をクリックし、規制に関する警告を送信します。 

### <a name="describe-the-alert"></a>警告の説明

1. 適切なフィールドに警告に関する情報を入力します。 必須フィールドは赤いアスタリスクで示されます。 次のテーブルでは、**警告の説明** ページのフィールドの詳細について説明します。

    <table >
            <tr>
                <td >
                <p><strong>フィールド</strong></p>
                </td>
                <td >
                <p><strong>説明</strong></p>
                </td>
            </tr>
            <tr>
                <td>
                <p>肩書き</p>
                </td>
                <td>
                <p>影響の区分を識別するために、内容を示すタイトルを入力します。 たとえば、<strong>2018 年 1 月 1 日時点での請求書ドキュメントの変更</strong>を入力します。</p>
                </td>
            </tr>
            <tr>
                <td>
                <p>説明</p>
                </td>
                <td>
                <p>法律の簡単な概要を入力します。 説明は、エンタープライズ リソース プランニング (ERP) に関連する問題に重点を置く必要があります。これにより、ユーザーは、最初に法律を読むことなく、要件を高いレベルで理解することができます。 </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>国</p>
                </td>
                <td>
                <p>法律が適用される国または地域を選択します。 </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>業</p>
                </td>
                <td>
                <p>要件が特定の業界にのみ適用される場合は、業界を選択します。 たとえば、<strong>公的機関</strong>、<strong>コマース</strong>、または<strong>製造</strong>を選択します。 </p><br/>            </td>
            </tr>
            <tr>
                <td>
                <p>機能リファレンス</p>
                </td>
                <td>
                <p>分かっている場合は、機能リファレンスを入力します。</p>
                </td>
            </tr>
            <tr>
                <td>
                <p>法執行日</p>
                </td>
                <td>
                <p>影響を受ける顧客が法律に準拠し始める必要がある日付を選択します。  </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>政府発表日</p>
                </td>
                <td>
                <p>所轄官庁が変更を発表した日付を選択します。 </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>最新の提出日</p>
                </td>
                <td>
                <p>新しいまたは変更されたレポートの最初の提出期限を選択します。     </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>法律へのリンク </p>
                </td>
                <td>
                <p>発行済みの法律、解釈規定、実装ガイダンスまたはユーザーが要件を理解または実装するのに役立つその他の有用な文書へのリンクを 1 つ以上入力します。</p>
                </td>
            </tr>
            <tr>
                <td>
                <p>屋号</p>
                </td>
                <td>
                <p>警告を送信しているユーザーの会社名を入力します。         </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>連絡先名</p>
                </td>
                <td>
                <p>警告を送信している担当者の名前を入力します。     </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>連絡先の電子メール</p>
                </td>
                <td>
                <p>警告の送信者の電子メール アドレス。   </p>
                </td>
            </tr>
            <tr>
                <td>
                <p>業務プロセス</p>
                </td>
                <td>
                <p><strong>警告の送信</strong> ウィザードで選択したビジネスプロセス。</p>
                </td>
            </tr>
            <tr>
                <td>コメント</td>
                <td>
                <p>ユーザーが要件を理解または実装するのに役立つ追加情報を入力します。 <strong>送信</strong>をクリックしてコメントを保存します。 複数のコメントを追加でき、個別に提出する必要があります。 コメントは追加された順に保存されます。 </p>
                </td>
            </tr>
            <tr>
                <td> アタッチメント </td>
                <td> <p><strong>アップロード</strong> ボタンをクリックし、添付ファイルとして追加するファイルを選択して参照します。 ファイルを選択した後、アップロードされリンクされたファイルとして表示されます。 各サイズが 5 MB のファイルを、最大 3 つ追加することができます。 添付されたファイルを削除するには、ファイルのタイトルの下にある <strong>削除</strong> をクリックします。 <strong>注記:</strong> 添付ファイルは公開されているものでなければなりません。 これらは妥当性や顧客固有/パートナー固有のものではありません。</p>
                </td>
            </tr>
    </table>

2.  すべての情報入力が完了したら、同意チェック ボックスを選択します (**この規制の警告を送信することで、Microsoft がこの警告に関する追加の情報を入手する目的で私に連絡することに同意します。Microsoft のプライバシーに関する声明**) 。 チェック ボックスを選択すると、**送信** ボタンが使用できるようになります。
3.  警告を保存して送信するには、**送信** をクリックします。

すべての必要な情報を持っていない場合、または警告を送信する準備が整っていない場合は、部分的に完了した警告を保存することができます。

### <a name="confirm-your-submission"></a>送信を確認する

-   警告が正常に送信されると、確認メッセージが表示されます。 **完了** をクリックし、ウィザードを終了します。
-   送信する前に警告を保存すると、警告 ID が生成され、警告が保存されたという確認を受け取ります。

## <a name="track-the-status-of-regulatory-features-in-issue-search"></a>問題検索の規制機能の状態を追跡する
LCS で問題検索を使用して計画済みおよびリリース済みの規制フィーチャー、および任意の関連ローカライズ ドキュメント、証明、およびレポートを見つけることができます。 検索を規制機能に絞り込むには、次のフィルターを使用します。

-   **カテゴリ** - **規制機能** のみを選択します。
-   **国/地域** - **&gt;** をクリックして、目的の国/地域を選択します。

検索範囲をさらに絞り込むには、次の追加フィルターを適用します

-   **製品** - 興味のある製品と製品のバージョンを選択します。
-   **ステータス** - 特定のステータスを選択してください。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
