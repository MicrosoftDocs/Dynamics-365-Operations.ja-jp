<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売トランザクションの整合性チェック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Retail の小売トランザクションの整合性チェック機能について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売トランザクションの整合性チェック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.3 に導入された小売トランザクションの整合性チェック機能について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">整合性チェックは、矛盾するトランザクションを特定し、明細書転記プロセスによって収集される前に隔離します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">明細書が Microsoft Dynamics 365 for Retail に転記される際、小売トランザクション テーブルのデータ不整合が原因で転記が失敗する場合があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">データの不整合は、販売時点管理 (POS) アプリケーションでの予期しない問題によって、またはトランザクションがサード パーティの POS システムから正しくインポートされなかった場合に起こります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">こうした不整合は、次のような形で表れます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘッダー テーブルのトランザクションの合計が、明細行のトランザクションの合計と一致しない。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘッダー テーブルの行数が、トランザクション テーブルの行数と一致しない。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘッダー テーブルの税金額が、明細行の税金額と一致しない。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細書転記プロセスによって矛盾したトランザクションが収集されると、矛盾した売上請求書と支払仕訳帳が作成され、その結果、明細書転記プロセス全体が失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような状態になった明細書を修正するには、複数のトランザクション テーブルにわたって複雑なデータ修正を行わなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売トランザクションの整合性チェックには、こうした問題を防ぎます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、トランザクションの整合性チェックを使用した転記プロセスを説明しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>小売トランザクションの整合性チェックを使用した明細書転記プロセス<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>小売トランザクションの整合性チェックを使用した明細書転記プロセス<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">バッチ処理 <bpt id="p1">**</bpt>店舗トランザクションを検証する<ept id="p1">**</ept> では、次のシナリオで小売トランザクション テーブルの整合性をチェックします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>顧客 ID<ept id="p1">**</ept> - 小売トランザクション テーブルの顧客 ID が HQ 顧客マスターに存在することを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>行数<ept id="p1">**</ept> - トランザクション ヘッダー テーブルにキャプチャされた明細行の数が、販売トランザクション テーブルの明細行の数と一致していることを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>税込み価格<ept id="p1">**</ept> – <bpt id="p2">**</bpt>税込み価格<ept id="p2">**</ept> パラメーターがトランザクション明細行間で一貫していることを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>総額<ept id="p1">**</ept> – ヘッダーの総額が明細行の正味金額と税額の合計であることを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>正味金額<ept id="p1">**</ept> – ヘッダーの総額が明細行の正味金額と税額の合計であることを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>過少支払または過剰支払<ept id="p1">**</ept> – ヘッダーの総額と支払額の差が最大過少支払/過剰支払コンフィギュレーションを超えていないことを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>割引金額<ept id="p1">**</ept> – 割引テーブルの割引金額と小売トランザクション明細行のテーブルの割引金額が一致していること、およびヘッダーの割引金額が明細行の割引金額の合計であることを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>明細行割引<ept id="p1">**</ept> – トランザクション明細行の明細行割引が、トランザクション明細行に対応する割引テーブルのすべての明細行の合計であることを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ギフト カード品目<ept id="p1">**</ept> – Retail ではギフト カード品目の返品はサポートされません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、ギフト カードの残高をキャッシュ アウトできます。キャッシュ アウト明細行の代わりに返品明細行としてギフト カード品目を処理すると、明細書の転記プロセスに失敗します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ギフト カード品目の検証プロセスにより、小売トランザクション テーブルの返品ギフト カード明細行品目のみがギフト カードのキャッシュ アウト明細行であることが保証されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>負の価格<ept id="p1">**</ept> – 負の価格のトランザクション明細行が存在しないことを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>品目およびバリアント<ept id="p1">**</ept> – トランザクション明細行の品目およびバリアントが品目およびバリアント マスター ファイルに存在することを検証します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">整合性チェックの設定</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>小売 <ph id="ph1">\&gt;</ph> 小売 IT <ph id="ph2">\&gt;</ph> POS 転記<ept id="p1">**</ept> でバッチ処理「店舗トランザクションを検証する」を構成し、定期処理を実行します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ ジョブは、「明細書をバッチ計算する」や「明細書をバッチ転記する」の設定方法と同様に、店舗の組織階層を基にスケジュールできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このバッチ処理が 1 日に複数回実行されるように設定し、すべての P ジョブ実行の最後に実行されるようにスケジュールすることをおすすめします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証プロセスの結果</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ処理による検証確認の結果は、適切な小売トランザクションにタグ付けされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売トランザクション レコードの <bpt id="p1">**</bpt>検証ステータス<ept id="p1">**</ept> フィールドは <bpt id="p2">**</bpt>成功<ept id="p2">**</ept> または <bpt id="p3">**</bpt>エラー<ept id="p3">**</ept> に設定され、検証が最後に実行された日付が <bpt id="p4">**</bpt>最後の検証日時<ept id="p4">**</ept> フィールドに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証エラーを詳しく説明したエラー テキストを表示するには、関連する小売店舗のトランザクション レコードを選択し、<bpt id="p1">**</bpt>検証エラー<ept id="p1">**</ept> ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証に失敗したトランザクション、およびまだ検証されていないトランザクションは、明細書に取り込まれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「明細書の計算」のプロセス中に、明細書に含むことができたが含まれなかったトランザクションがある場合、ユーザーに通知されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証エラーが検出された場合、Microsoft サポートに問い合わせることでしかエラーは修正できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来のリリースでは、エラーとなったレコードをユーザー インターフェイスを通じて修正するための機能が追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更履歴を追跡するためのログおよび監査機能も利用可能になる予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">より多くのシナリオをサポートするための検証ルールは、将来のリリースで追加されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>