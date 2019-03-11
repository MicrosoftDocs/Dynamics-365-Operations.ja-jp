---
title: 顧客エンティティへの拡張プロパティの追加
description: このチュートリアルでは、拡張プロパティを使用してエンティティを拡張する方法を示します。
author: mugunthanm
manager: AnnBe
ms.date: 06/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 196163
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b135cde1a902f6c3797bb2371975f0a09e48ccce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369390"
---
# <a name="add-extension-properties-to-customer-entities"></a>顧客エンティティへの拡張プロパティの追加

[!include [banner](../includes/banner.md)]

このチュートリアルでは、拡張プロパティを使用してエンティティを拡張する方法を示します。 

このチュートリアルでは、エンティティが Microsoft 365 for Retail で拡張され、Retail とチャネル データベースの両方で保持されます。 これにより、販売時点管理 (POS) ユーザー インターフェイス (UI) で値にアクセスできます。 また、新しい値は、Commerce Data Exchange (CDX) 取引サービスを介して Dynamics AX に同期的に書き込まれます。 拡張機能プロパティは自動的にフローするため、Commerce Runtime または Retail サーバーに必要なカスタマイズはありません。 フォーム、テーブル、Real-time Service (RTS) クライアント、CDX、チャネル データベース、POS (Retail Modern POS およびクラウド POS の両方) の変更が必要です。 このチュートリアルでは、オフライン モードをサポートしていません。

<a name="create-a-new-dynamics-ax-project"></a>新しい Dynamics AX プロジェクトを作成します
--------------------------------

1.  **RetailCustPreference** という名前の新しいテーブルを作成し、CustTable テーブルを参照します。
2.  Microsoft Visual Studio を起動します。
3.  新しいモデルおよびプロジェクトを作成します。 **Dynamics AX** メニューで、**モデル管理** &gt; **モデルの作成** をクリックします。
4.  USR レイヤーに新しいモデルを作成し、**次へ**をクリックします。
5.  既存の ApplicationSuite パッケージへモデルを追加します。 **次へ**をクリックし、**完了**の順にクリックします。
6.  プロジェクト名を入力し、**OK** をクリックします。
7.  ソリューション エクスプローラーで、新しいプロジェクトを右クリックします。 **追加** &gt; **新しい品目** を選択し、**RetailCustPreference** という新しいテーブルを追加します。
8.  プロジェクトで、**RetailCustPreference** をダブルクリックしてテーブル デザイナーを開きます。
9.  **EmailOptIn** という名前の新しい列挙フィールドを作成し、**Enum Type** プロパティーを **NoYes** に設定します。
10. **AccountNum** という名前の新しい文字列フィールドを作成します。 フィールドの拡張データ型を **CustAccount** に設定し、**Mandatory** プロパティを **Yes** に設定します。
11. CustTable テーブルを使用して新しいリレーションを作成し、**RetailCustPreference.AccountNum** と **CustTable.AccountNum** の間に新しい通常のリレーションを追加します。
12. 変更を保存します。
13. ソリューション エクスプローラーで、プロジェクトを右クリックしてから**プロパティ**を選択します。
14. **ビルドでデータベースを** **同期** チェック ボックスをオンにします。
15. プロジェクトを右クリックし、**ビルド** を選択して新しいコードを作成およびデータベースを同期します。
16. ビルドが完了したら、プロジェクトのプロパティに戻り、**ビルドでの** **データベースの同期** チェック ボックスをオフにします。

## <a name="update-the-custtable-form"></a>CustTable フォームの更新
1.  アプリケーション エクスプローラーで、**ユーザー インターフェイス** &gt; **フォーム** &gt; **CustTable** を選択します。 **CustTable** を右クリックし、**拡張子の作成** を選択します。
2.  これで、プロジェクトに **CustTable.Extension** という名前の新しい要素が含まれます。 フォーム デザイナーを開くには、要素をダブルクリックします。
3.  **RetailCustPreference** という名前の新しいデータ ソースを追加し、設定し、**リンク タイプ** プロパティを **OuterJoin** に設定します。
4.  **CustTable** フォームの **小売**タブ ページで、**顧客の優先**という名前の新しいグループを追加し、**キャプション**プロパティに**顧客の優先**を設定します。
5.  **CustomerPreference** グループの **RetailCustPreference** テーブルに、**EmailOptIn** という名前の新しいチェック ボックス フィールドを追加します。
6.  **CustTable\_Extension** という名前の新しいクラスを追加します。 コード エディターで、次のコードを追加します。

        public static class CustTable_Extension
        {
            [FormDataSourceEventHandler(formDataSourceStr(CustTable, CustTable), FormDataSourceEventType::ValidatingWrite)]
            public static void foo(FormDataSource fds, FormDataSourceEventArgs e)
            {
                FormRun                             form = fds.formRun();
                CustTable                           custTable = fds.cursor() as CustTable;
                RetailCustPreference                retailCustPreference = form.dataSource(formDataSourceStr(CustTable, RetailCustPreference)).cursor() as RetailCustPreference;
                retailCustPreference.AccountNum     = custTable.AccountNum; form.dataSource(formDataSourceStr(CustTable, RetailCustPreference)).write(); 
            } 
        }

7.  すべての変更を保存し、プロジェクトを再度ビルドします。
8.  **iisreset** を実行します。
9.  Dynamics 365 for Retail で、**売掛金勘定** &gt; **共通** &gt; **顧客** &gt; **すべての顧客** の順にクリックします。
10. 顧客レコードを編集します。 **小売**クイック タブで、**電子メール申し込み**チェック ボックスをオンにし、変更を保存します。

## <a name="customize-the-existing-retailtransactionservice-class-so-that-it-handles-the-new-data-correctly"></a>新しいデータが正しく処理できるように、既存の RetailTransactionService クラスをカスタマイズします
1.  アプリケーション エクスプローラーで、**RetailTransactionService (sys)** クラスを右クリックしてから**カスタマイズ**を選択します。
2.  終了時に、次の 2 つの方法を追加します。

        /// <summary>
        /// Processes all Extension properties. This is a sample only. Should be re-factored into its own class for better reuse and better decoupling from RetailTransactionService
        /// </summary>
        /// <param name = "extensionProperties"></param>
        private static void processExtensionProperties(AccountNum accountNum, str extensionProperties)
        {
            XmlElement                  xmlElementExtensionProperties;
            XmlNodeList                 xmlListExtensionProperties;
            int                         i;
            XmlElement                  xmlElementExtensionProperty;
            str                         propertyName;
            str                         propertyValue;
            int                         emailOptInValue;
            if(extensionProperties != null && extensionProperties != '')
            {
                XmlDocument xmlExtensionProperties = new XmlDocument();
                xmlExtensionProperties.loadXml(extensionProperties);
                xmlElementExtensionProperties = xmlExtensionProperties.getNamedElement('ExtensionProperties');
                xmlListExtensionProperties = xmlElementExtensionProperties.childNodes();
                if (xmlListExtensionProperties)
                {
                    for (i = 0; i < xmlListExtensionProperties.length(); i++)
                    {
                        xmlElementExtensionProperty = xmlListExtensionProperties.item(i);
                        if(xmlElementExtensionProperty)
                        {
                            propertyName = xmlElementExtensionProperty.tagName();
                            propertyValue = xmlElementExtensionProperty.innerText();
                            switch(propertyName)
                            {
                                case "EMAILOPTIN":
                                    // update the EMAILOPTIN value
                                    if(propertyValue != null && propertyValue != '')
                                    {
                                        emailOptInValue = str2Int(propertyValue);
                                    }
                                    else
                                    {
                                        emailOptInValue = 0;
                                    }
                                    RetailTransactionService::updateOptIn(accountNum, emailOptInValue);
                                    break;
                                default:
                                    // do something else here...
                                    break; 
                            } 
                        } 
                    } 
                } 
            } 
        }

        /// <summary>
        /// Updates the customer email optin value. This is a sample only. Should be re-factored into its own class for better reuse and better decoupling from RetailTransactionService
        /// </summary>
        /// <param name = "accountnum"></param>
        /// <param name = "emailOptIn"></param>
        /// <returns></returns>
        private static container updateOptIn(AccountNum accountnum, int emailOptIn)
        {
            RetailCustPreference        retailCustPreference;
            boolean validUpdate = false;
            str error = "NO error";
            int fromLine;
            try
            {
                //Extensibility code for cust preference
                select forUpdate EmailOptIn from retailCustPreference  where  retailCustPreference.AccountNum == accountnum;
                if(retailCustPreference.RecId)
                {
                    //retailCustPreference.clear();
                    ttsBegin;
                    retailCustPreference.EmailOptIn = emailOptIn;
                    retailCustPreference.update();
                    ttscommit;
                }
                else
                {
                    retailCustPreference.clear();
                    retailCustPreference.AccountNum = accountNum;
                    retailCustPreference.EmailOptIn = emailOptIn;
                    retailCustPreference.insert();
                }
                validUpdate = true;
            }
            catch(Exception::Error)
            {
                ttsabort;
                error = RetailTransactionServiceUtilities::getInfologMessages(fromLine);
                RetailTracer::Error('RetailTransactionService', funcName(), error);
            }
            // Returning the status as a container
            return [validUpdate, error,retailCustPreference.AccountNum];
        }

3.  次のコードを末尾に追加して、**updateCustomerExt** メソッドを更新します。 (また、コードの最初の行に **customerContainer** の変数申告を追加します。)

        // the third element in container is the account number
        AccountNum accountNum = conPeek(customerContainer, 3);
        RetailTransactionService::processExtensionProperties(accountNum, extensionProperties);
        return customerContainer;

4.  プロジェクトをコンパイルします。

## <a name="configure-cdx-to-sync-the-new-table"></a>新しいテーブルを同期させる CDX をコンフィギュレーションします。
1.  Dynamics 365 for Retail で、**Retail** &gt; **設定** &gt; **小売用スケジューラ** &gt; **小売チャネル** **スキーマ** と移動し、新しいテーブルを追加してチャネル スキーマを編集します。
    1.  **チャネル テーブル**、**新規**の順にクリックします。
    2.  テーブルに **ax.RetailCustPreference** と名前を付けて保存します。
    3.  次のフィールドを追加します: **ACCOUNTNUM**、**DATAAREAID**、**EMAILOPTIN**、**RECID**。
    4.  **OK** をクリックします。

2.  **Retail** &gt; **設定** &gt; **小売用スケジューラ** &gt; **スケジューラ サブジョブ**の順に移動し、新しいサブジョブを作成します。
    1.  **Name** フィールドを **RetailCustPreference** に、**Description** フィールドを **RetailCustPreference** に置き換えます。
    2.  **チャネル テーブル名**フィールドを **ax.RetailCustPreference** に設定します。
    3.  **AX テーブル** フィールドを **RetailCustPreference** に設定します。
    4.  **フィールドの照合**をクリックします。
    5.  **保存** をクリックします。

3.  **小売** &gt; **設定** &gt; **小売用スケジューラ** &gt; **スケジューラ サブジョブ**、**顧客 - 1010** ジョブに新しいサブジョブを追加して、変更を保存します。
4.  **小売** &gt; **設定** &gt; **小売用スケジューラ** &gt; **小売チャンネル スキーマ**、**エクスポート、編集、** **新しい名前で保存**、**インポート**の順に移動し、CDX テーブル配送 XML を編集します。 両方の **CustTable** ノード内に、次の XML フラグメントを追加します。 (この XML フラグメントを追加することで、チャンネルと同期しているときに、このテーブルの変更を明示的に含めることになります。)

        <Table name="RetailCustPreference">
            <LinkGroup>
                <Link type="FieldMatch" fieldName="accountNum" parentFieldName="AccountNum" />
            </LinkGroup>
        </Table>

5.  **小売チャネル スキーマ** ページで、スキーマ名として **AX** を選択してから、**クエリの生成** をクリックします。

## <a name="channel-database"></a>チャネル データベース
開発用チャンネル データベースを手動で変更します。 実際の展開については、このトピックで後述の「実際の展開」を参照してください。 新しいテーブルを追加するには ChannelDBUpgrade.sql から正しいチャンネル データベースへスキーマの変更を適用する必要があります。

1.  \[crt\].\[CUSTOMERSVIEW\] の変更:
    -   UNION All の前に、選択する必要がある列のリストの最後に「, isnull(rcp.EMAILOPTIN, 0) as EMAILOPTIN」を追加します。
    -   UNION All の前に、「LEFT OUTER JOIN \[ax\].RETAILCUSTPREFERENCE rcp ON ct.ACCOUNTNUM = rcp.ACCOUNTNUM AND ct.DATAAREAID = rcp.DATAAREAID」を追加します。
    -   UNION All の後に、選択する必要がある列のリストの最後に、「, 0  as EMAILOPTIN」を追加します。
    -   ストアド プロシージャ \[crt\].\[CREATEUPDATECUSTOMER\] を変更します:

2.  行 「MERGE INTO \[ax\].DIRADDRESSBOOKPARTY」の直前に次のコードを追加します。

        MERGE INTO [ax].RETAILCUSTPREFERENCE
        USING (SELECT DISTINCT
        tp.PARENTRECID, tp.PROPERTYVALUE as [EMAILOPTIN], ct.ACCOUNTNUM, ct.DATAAREAID
        FROM @TVP_EXTENSIONPROPERTIESTABLETYPE tp
        JOIN [ax].CUSTTABLE ct on ct.RECID = tp.PARENTRECID
        WHERE tp.PARENTRECID <> 0 and tp.PROPERTYNAME = 'EMAILOPTIN') AS SOURCE
        ON [ax].RETAILCUSTPREFERENCE.RECID = SOURCE.PARENTRECID
            and [ax].RETAILCUSTPREFERENCE.DATAAREAID = SOURCE.DATAAREAID
            and [ax].RETAILCUSTPREFERENCE.ACCOUNTNUM = SOURCE.ACCOUNTNUM
        WHEN MATCHED THEN
        UPDATE SET [EMAILOPTIN] = source.[EMAILOPTIN]
        WHEN NOT MATCHED THEN
        INSERT
        (
            RECID
            ,DATAAREAID
            ,EMAILOPTIN
            ,ACCOUNTNUM
        )
        VALUES
        (
            SOURCE.PARENTRECID
            ,SOURCE.DATAAREAID
            ,SOURCE.EMAILOPTIN
            ,SOURCE.ACCOUNTNUM
        );
        SELECT @i_Error = @@ERROR;
        IF @i_Error <> 0
        BEGIN
        SET @i_ReturnCode = @i_Error;
        GOTO exit_label;
        END;

## <a name="verify-cdx"></a>CDX の確認
1.  完全な同期 (チャネル データ グループ) を使用して、1010 ジョブを実行します。
2.  ダウンロード セッションとチャネル データベースをチェックして、データが到着したことを確認します。(**適用済**として表示されます)。

**注記:** Commerce Runtime または Retail サーバーのカスタマイズは必要ありません。 拡張プロパティは自動的にフローされます。

## <a name="test-the-customizations-business-logic-by-using-the-retail-server-test-client"></a>Retail Server テスト クライアントを使用して、カスタマイズのビジネス ロジックをテスト
1. プロジェクトを **RetailSdk\\SampleExtensions\\RetailServer\\Extensions.TestClient** で開いて、コンパイルし、実行します。
2. **新しく有効化**ボタンの横にあるフィールドに、Retail サーバー URL を入力してから、**新しく有効化**をクリックします。
3. デバイスを入力し、ID を登録し、次に**アクティブにする**をクリックします。
4. 登録権限を持つ Microsoft Azure Active Directory (Azure AD) の資格情報を入力し、**OK** をクリックします。
5. テスト クライアントが登録されているデバイスを表示するまで待機します。
6. サインイン ボタンをクリックし、作業者の資格情報を使用してサインインします。
7. **Sdk テスト**をクリックします。 このボタンは、**EmailOptIn** 拡張プロパティが適用された顧客を保存する新しい機能を呼び出します。
8. Dynamics AX またはデータベースで、顧客の <strong>EmailOptIn</strong> 値が正しく保存されていることを確認します。 <strong>注記: **エラー/ログを含むコンソールを表示するには、**デバッグ</strong>ボタンを使用します。

## <a name="extend-modern-pos"></a>Modern POS 拡張
1.  **ModernPos.sln** ソリューションを開きます。
2.  ソリューションの **BEGIN SDKSAMPLE\_CUSTOMERPREFERENCES** をグローバル検索します。
3.  見つけたすべての場所でコードを有効にし、再コンパイルします。 リソース ファイルが 1 つだけ必要です。 必要なロケールを選択することができます。
4.  Modern POS を実行し、新しい顧客を作成できることを確認します。 既存の顧客が更新されると、チャネル データベースと Dynamics AX データベースの両方でフラグが正しく更新される必要があります。

## <a name="live-deployment"></a>実際の展開
1.  データベース フォルダーにチャネル データベースの変更ファイルを追加し、**customization.settings** に登録します。
2.  Retail SDK ソリューションに **msbuild** を実行します。 すべてのパッケージにはすべての適切な変更があります。
3.  Microsoft Dynamics Lifecycle Services (LCS) を使用するか手動でパッケージを展開します。




