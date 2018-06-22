---
title: "Dynamics 365 for Finance and Operations、Enterprise edition プラットフォーム更新プログラム 11 (2017 年10 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 11 における新機能または変更された機能について説明します。 このバージョンは 2017 年 10 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 10/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform update 11
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 386a4cbadcec8d74309c6cac26a8620f8425a9fa
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-enterprise-edition-platform-update-11-october-2017"></a><span data-ttu-id="8d8b5-104">Dynamics 365 for Finance and Operations、Enterprise edition プラットフォーム更新プログラム 11 (2017 年10 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="8d8b5-104">What's new or changed in Dynamics 365 for Finance and Operations, Enterprise edition platform update 11 (October 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d8b5-105">このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 11 における新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-105">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations, Enterprise edition platform update 11.</span></span> <span data-ttu-id="8d8b5-106">このバージョンは 2017 年 10 月にリリースされ、ビルド番号は 7.0.4679.35176 です。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-106">This version was released in October 2017 and has a build number of 7.0.4679.35176.</span></span>

<span data-ttu-id="8d8b5-107">新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-107">Go to the [Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to find supplemental information about new features and learn more about what new features are in development.</span></span> <span data-ttu-id="8d8b5-108">プラットフォーム更新プログラム 11 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4047244&bugId=3869536&qc=310ad7de90642ce961cc3f51358f3b40788c975dec466891d0fcc17c13145f56) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-108">For information about the bug fixes included in Platform update 11, log in to Lifecycle Services (LCS) and view this [KB article](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4047244&bugId=3869536&qc=310ad7de90642ce961cc3f51358f3b40788c975dec466891d0fcc17c13145f56).</span></span>

## <a name="attachment-presence-and-document-count-indicator"></a><span data-ttu-id="8d8b5-109">添付ファイルのプレゼンスとドキュメント数のインジケータ</span><span class="sxs-lookup"><span data-stu-id="8d8b5-109">Attachment presence and document count indicator</span></span>  
<span data-ttu-id="8d8b5-110">レコードを表示するとき、システムは、添付ファイル ボタンに数を表示することによって、そのレコードの添付ファイルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-110">When viewing a record, the system will indicate the number of attachments on that record by showing a count on the Attachments button.</span></span> <span data-ttu-id="8d8b5-111">この数は、添付ファイルの詳細フォームに移動せずに、レコードに関連付けられた添付ファイルがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-111">This number will indicate that there are attachments associated with the record, without having to navigate to the attachment details form.</span></span> <span data-ttu-id="8d8b5-112">カウントには 9 つまでの添付ファイルが表示され、9 以上の添付ファイルが「9+」として表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-112">The count will show up to 9 attachments, with more than 9 attached documents being represented as “9+”.</span></span> <span data-ttu-id="8d8b5-113">詳細については、[ドキュメント管理のコンフィギュレーション](../organization-administration/configure-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-113">For more information, see [Configure document management](../organization-administration/configure-document-management.md).</span></span>

## <a name="auditing"></a><span data-ttu-id="8d8b5-114">監査</span><span class="sxs-lookup"><span data-stu-id="8d8b5-114">Auditing</span></span>
<span data-ttu-id="8d8b5-115">ユーザーのログインとサインアウトの監査が Finance and Operations で有効になりました。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-115">Auditing of user sign in and sign out is now enabled in Finance and Operations.</span></span> <span data-ttu-id="8d8b5-116">ユーザーがアプリケーションにサインインまたはサインアウトすると、システムログが記録されます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-116">The system logs when a user signs in or out of the application.</span></span> <span data-ttu-id="8d8b5-117">ユーザーのセッションが期限切れまたは終了する場合でも、サインアウトが記録されます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-117">A sign out is logged even if the user's session expires or ends.</span></span>

<span data-ttu-id="8d8b5-118">システム管理者またはセキュリティー管理者は、**ユーザー ログ** ページ (**システム管理** > **照会** > **ユーザー ログ**) に移動して監査ログにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-118">A system administrator or security administrator can access the audit logs by going to the **User log** page (**System administration** > **Inquiries** > **User log**).</span></span>

## <a name="bring-your-own-database-byod-support-for-delete-operations"></a><span data-ttu-id="8d8b5-119">削除操作のための自分のデータベースの持ち込み (BYOD) のサポート</span><span class="sxs-lookup"><span data-stu-id="8d8b5-119">Bring your Own Database (BYOD) support for delete operations</span></span>

<span data-ttu-id="8d8b5-120">自分のデータの持ち込みストア (BYOD) は、顧客が既存のデータ ウェアハウスと Finance and Operations のデータを統合するために使用する機能です。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-120">Bring your own data store (BYOD) is a feature that’s used by customers to integrate data from Finance and Operations with existing data warehouses.</span></span> <span data-ttu-id="8d8b5-121">BYOD を使用するとデータを顧客の SQL Azure データベースに段階的にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-121">BYOD allows you to incrementally export data into a customer’s SQL Azure database.</span></span>
<span data-ttu-id="8d8b5-122">差分エクスポート フィーチャーは変更の反映に理想的ですが、一般的に初期データの設定に使用される完全なエクスポートもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-122">While an incremental export feature is ideal for propagating changes, we will also support full export, which is typically used for initial data population.</span></span>
<span data-ttu-id="8d8b5-123">増分操作は、出力先のデータベースへの挿入および更新操作に反映されます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-123">Incremental operation propagates insert and update operations to the destination database.</span></span> <span data-ttu-id="8d8b5-124">この追加機能では、ソース内の対応するレコードが削除された場合、BYOD 差分更新操作により出力先データベース内のレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-124">With this addition, BYOD incremental refresh operations delete records in the destination database if corresponding records are deleted in source.</span></span>

## <a name="cloud-and-edge-elements"></a><span data-ttu-id="8d8b5-125">クラウドおよびと Edge の要素</span><span class="sxs-lookup"><span data-stu-id="8d8b5-125">Cloud and Edge elements</span></span> 
<span data-ttu-id="8d8b5-126">テーブル、ビュー、データ エンティティ、メニュー項目、およびサービス操作には、**運用ドメイン** および **サブスクライバー アクセス レベル** というメタデータ プロパティが追加されています。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-126">The metadata properties, **Operational domain** and **Subscriber access level** have been added for tables, views, data entities, menu items, and service operations.</span></span> <span data-ttu-id="8d8b5-127">[クラウドおよびエッジの配置](https://community.dynamics.com/b/msftdynamicsblog/archive/2017/02/23/the-right-cloud-option-for-your-business) をサポートするには新しいメタデータ プロパティが必要で、Microsoft Visual Studio で表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-127">The new metadata properties are needed to support [Cloud and Edge deployments](https://community.dynamics.com/b/msftdynamicsblog/archive/2017/02/23/the-right-cloud-option-for-your-business), and are visible in Microsoft Visual Studio.</span></span> 

<span data-ttu-id="8d8b5-128">また、同じで目的で**配置**、**DeploymentAccessibleCompany**、**NumberSequenceDeployments** の 3 つのテーブルが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-128">Additionally, three tables, **Deployment**, **DeploymentAccessibleCompany**, and **NumberSequenceDeployments** have been added, for the same purpose.</span></span> 

<span data-ttu-id="8d8b5-129">現時点では、新しいプロパティとテーブルを取得する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-129">At this time, you are not required to uptake the new properties and tables.</span></span>

## <a name="copy-legal-entity-configurations-to-a-new-legal-entity"></a><span data-ttu-id="8d8b5-130">法人のコンフィギュレーションを新しい法人にコピーする</span><span class="sxs-lookup"><span data-stu-id="8d8b5-130">Copy legal entity configurations to a new legal entity</span></span>

<span data-ttu-id="8d8b5-131">新しい会社が必要になると、ユーザーは既存の法人組織の設定を新しい会社にコピーすることで、時間を節約し、潜在的なエラーを削減することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-131">As new companies are needed, users will be able to save time and potential errors by copying an existing legal entity’s setup to the new company.</span></span> <span data-ttu-id="8d8b5-132">これにより、新しい場所でのオンボードが迅速になり、企業のゴールデン テンプレート デザインとの一貫性を保つことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-132">This will allow the onboarding of a new location to be quick and consistent with the company’s golden template design.</span></span>

## <a name="development-and-customization---field-groups---extension-of-another-extension"></a><span data-ttu-id="8d8b5-133">開発およびカスタマイズ - フィールド グループ - 他の拡張の拡張機能</span><span class="sxs-lookup"><span data-stu-id="8d8b5-133">Development and customization - Field groups - Extension of another extension</span></span>

<span data-ttu-id="8d8b5-134">TableExtension1 と TableExtension2 の 2 つのモデルに 2 つの拡張機能を持つテーブル (Table1) があるとします。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-134">Consider you have a table (Table1) that has two extensions in 2 separate models: TableExtension1 and TableExtension2.</span></span> <span data-ttu-id="8d8b5-135">TableExtension1 には、新しいフィールド グループ (NewFieldGroup1) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-135">TableExtension1 contains a new field group (NewFieldGroup1).</span></span> <span data-ttu-id="8d8b5-136">TableExtension2 を使用すると、NewFieldGroup1 にフィールドを追加できますようになります。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-136">Using TableExtension2, you can now add a field to NewFieldGroup1.</span></span> <span data-ttu-id="8d8b5-137">フォーム拡張子に NewFieldGroup1 を追加する場合は、実行時にユーザー インターフェイスですべてのフィールドが認識され、レンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-137">If you add NewFieldGroup1 to a form extension, all fields are recognized and rendered at runtime by the user interface.</span></span> <span data-ttu-id="8d8b5-138">この機能は、Platform update 11 以前には利用できませんでした。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-138">This functionality was not available prior to Platform update 11.</span></span>

## <a name="development-and-customization---support-for-display-and-edit-methods-in-class-extensions"></a><span data-ttu-id="8d8b5-139">開発およびカスタマイズ - クラス拡張の表示と編集メソッドのサポート</span><span class="sxs-lookup"><span data-stu-id="8d8b5-139">Development and customization - Support for display and edit methods in class extensions</span></span>

<span data-ttu-id="8d8b5-140">クラスの拡張機能 (テーブル クラスの拡張機能) を使用して表示を定義しメソッドを編集することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-140">You can now use class extensions (table class extensions) to define display and edit methods.</span></span> <span data-ttu-id="8d8b5-141">次の例は、これを示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-141">The following example illustrates this.</span></span>

<span data-ttu-id="8d8b5-142">LedgerJournalTransAccrual テーブルの拡張機能作成し、**MyStringField1** という名前の新しい文字列フィールドをテーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-142">Create an extension of the table LedgerJournalTransAccrual and add a new string field named **MyStringField1** to the table.</span></span> <span data-ttu-id="8d8b5-143">テーブル クラス LedgerJournalTransAccrual を次のように拡張します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-143">Augment the table class LedgerJournalTransAccrual as follows.</span></span>

```
[ExtensionOf(tableStr(LedgerJournalTransAccrual))]  
final class MyLedgerJournalTransAccrual_Extension  
{  
    [SysClientCacheDataMethodAttribute(true)]  
    public static display LedgerJournalAccountName
MyLedgerAccountName(LedgerJournalTransAccrual \_ledgerJournalTransAccrual)  
    {  
        return \_ledgerJournalTransAccrual.MyStringField1 + "Hello";  
    }

}
```

<span data-ttu-id="8d8b5-144">新しいフィールド グループを **MyLedgerAccountName** のテーブル拡張機能に追加し、フィールド グループの表示データ フィールドとしてメソッド **MyLedgerAccountName** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-144">Add a new field group to the table extension of **MyLedgerAccountName** and select the method **MyLedgerAccountName** as a display data field in the field group.</span></span> 

1.  <span data-ttu-id="8d8b5-145">新しいフィールド グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-145">Add a new field group.</span></span>

2.  <span data-ttu-id="8d8b5-146">フィールドグループに新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-146">Add a new field to the field group.</span></span>

3.  <span data-ttu-id="8d8b5-147">**データ フィールド** プロパティを **LedgerJournalTransAccrual_Extension::MyLedgerAccountName** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-147">Set the **Data Field** property to **LedgerJournalTransAccrual_Extension::MyLedgerAccountName**.</span></span> <span data-ttu-id="8d8b5-148">(それを入力するか、**データ フィールド** ドロップダウン リストから選択することができます)。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-148">(You can type it in or select it from the **Data Field** drop-down list).</span></span>

## <a name="development-and-customization---support-for-field-arrays-in-table-extensions"></a><span data-ttu-id="8d8b5-149">開発およびカスタマイズ - テーブル拡張のフィールド配列のサポート</span><span class="sxs-lookup"><span data-stu-id="8d8b5-149">Development and customization - Support for field arrays in table extensions</span></span>

<span data-ttu-id="8d8b5-150">テーブルを拡張し、テーブル拡張部に新しいフィールドを追加するとき、新しいフィールドが配列の EDT タイプの場合、X++ コードから EDT 配列フィールドにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-150">When you extend a table and add a new field to the table extension, if the new field is of type EDT that is an array, you can now access EDT array fields from X++ code.</span></span> <span data-ttu-id="8d8b5-151">これを実行する方法の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-151">Here is an example of how to do this.</span></span>

1.  <span data-ttu-id="8d8b5-152">テーブル拡張子を作成します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-152">Create a table extension.</span></span>

2.  <span data-ttu-id="8d8b5-153">テーブル拡張機能に新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-153">Add a new field to the table extension.</span></span>

3.  <span data-ttu-id="8d8b5-154">配列である EDT にフィールドのタイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-154">Set the field type to an EDT that is an array.</span></span>

4.  <span data-ttu-id="8d8b5-155">X++ では新しい拡張子フィールドを次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-155">Use the new extension field in X++ as follows.</span></span>

```
A table1;

table1.EDTArrayField1[1] = ‘text1’;  
table1.EDTArrayField1[2] = ‘text2’;  
table1.EDTArrayField1[3] = ‘text3’;  
// perform insert or update operations here on table 1
```

## <a name="development-and-customization---use-edt-extensions-to-customize-number-of-decimals"></a><span data-ttu-id="8d8b5-156">開発およびカスタマイズ - EDT 拡張機能を使用して小数点以下桁数をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="8d8b5-156">Development and customization - Use EDT extensions to customize number of decimals</span></span>

<span data-ttu-id="8d8b5-157">EDTReal 型の拡張データ型の拡張機能を使用するとき、小数点精度の変更を確認できます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-157">When you use an extension of an extended data type of type EDTReal, you can know change the decimal point precision.</span></span> <span data-ttu-id="8d8b5-158">展開している EDT 要素が持っている**番号の小数点以下が拡張可能な**プロパティが true に設定されている場合、この EDT の拡張機能を作成でき、**小数点以下なし**プロパティを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-158">If the EDT element you are extending has the property **Number of Decimals is Extensible** set to True, you can create an extension of this EDT and modify the **No of Decimals** property.</span></span> <span data-ttu-id="8d8b5-159">これにより、開発者はタイプ EDTReal の EDT の小数点精度をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-159">This allows developers to customize the decimal point precision of an EDT of type EDTReal.</span></span> <span data-ttu-id="8d8b5-160">現在のプラットフォーム更新プログラム 11 では、次の EDT で小数点の拡張が可能です。量および AmountMST。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-160">As of Platform update 11, the following EDTs allow decimal point extension: Amount and AmountMST.</span></span>

## <a name="multiple-document-reports-sent-as-a-zip-file-to-streamline-delivery"></a><span data-ttu-id="8d8b5-161">配送を簡素化するために .zip ファイルとして送信する複数のドキュメント レポート</span><span class="sxs-lookup"><span data-stu-id="8d8b5-161">Multiple document reports sent as a .zip file to streamline delivery</span></span>

<span data-ttu-id="8d8b5-162">このフレームワークは、レポート セッションがダウンロード用の複数の文書を生成するシナリオをよりよく扱うように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-162">The framework has been extended to better handle scenarios where reporting sessions produce multiple documents for download.</span></span> <span data-ttu-id="8d8b5-163">セキュリティ上の事前措置として、 Dynamics 365 for Finance and Operations サービスは複数のファイルをブラウザにダウンロードするシナリオの処理方法を調整しました。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-163">As a security precaution, the Dynamics 365 for Finance and Operations service has adjusted how to handle scenarios that download multiple files to the browser.</span></span> <span data-ttu-id="8d8b5-164">複数のドキュメントを次々と受信するのではなく、ドキュメントは 1 つの .zip ファイルにパッケージ化してダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-164">Instead of receiving multiple documents, one after another, the documents will be packaged and downloaded in a single .zip file.</span></span> <span data-ttu-id="8d8b5-165">これは、顧客取引明細書や督促状などの複数のドキュメントを生成する既存のレポートに影響します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-165">This will affect existing reports that produce multiple documents such customer account statements and collection letters.</span></span>

## <a name="resource-governor-manages-server-workloads"></a><span data-ttu-id="8d8b5-166">リソース ガバナーは、サーバー ワークロードを管理します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-166">Resource governor manages server workloads</span></span>

<span data-ttu-id="8d8b5-167">リソース ガバナーは、システム管理者の管理オーバーヘッドを削減するコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-167">Resource governor is a component that reduces the management overhead for a system administrator.</span></span> <span data-ttu-id="8d8b5-168">Finance and Operations にはバッチおよび処理タスクが含まれ、高速計算処理能力があります。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-168">Finance and Operations contains batch and processing tasks that are compute intensive.</span></span> <span data-ttu-id="8d8b5-169">複数の転記ジョブがある月末のワークロードなど、業務の必要性に応じて多くのジョブをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-169">Users can schedule many jobs as the business demands dictate, such as the month-end workload where there are multiple posting jobs.</span></span>
<span data-ttu-id="8d8b5-170">これらの計算処理はサーバーを占有しますが、フロント オフィス プロセスなどの対話型オペレーションは、パフォーマンスの低下なしに実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-170">While these compute processes occupy the server, interactive operations such as front-office processes, continue to run without any degradation of performance.</span></span>

<span data-ttu-id="8d8b5-171">リソース ガバナーは、SQL Azure データベースから提供される組み込みのリソース ガバナンス サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-171">Resource governor uses the built-in resource governance services offered by SQL Azure database.</span></span> <span data-ttu-id="8d8b5-172">Dynamics 365 for Finance and Operations ランタイム サービスでは、突然の計算スパイクがある場合、SQL Azure データベースは低下しないように対話型プロセスとバッチ プロセス (ほとんどの計算が実行される場所) の両方にクォータを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8d8b5-172">Dynamics 365 for Finance and Operations Runtime service allocates quotas for interactive, as well as batch processes, so that SQL Azure database (where most of the compute is performed) does not degrade if there are sudden compute spikes.</span></span>

