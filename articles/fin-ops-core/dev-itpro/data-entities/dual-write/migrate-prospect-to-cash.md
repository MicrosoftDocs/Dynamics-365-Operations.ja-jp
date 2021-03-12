---
title: データ統合からデュアル書き込みへの見込顧客の現金データへの移行
description: このトピックでは、データ統合からデュアル書き込みへの見込顧客の現金データへの移行方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f1478f0246e7f1ff8bd72232cbaf4c2034cf4edb
ms.sourcegitcommit: 6af7b37b1c8950ad706e684cc13a79e662985b34
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/14/2021
ms.locfileid: "4959849"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>データ統合からデュアル書き込みへの見込顧客の現金データへの移行

[!include [banner](../../includes/banner.md)]

データ統合からデュアル書き込みへの見込顧客の現金データへ移行するには、次の手順に従ってください。

1. 見込顧客から現金データの統合ジョブを実行して、最終的な完全同期を 1 つ実行します。 これにより、両方のシステム (Finance and Operations アプリと Customer Engagement アプリ) がすべてのデータが確実に設定されます。
2. データが失われる可能性を防ぐには、Microsoft Dynamics 365 Sales から Excel ファイルまたはコンマ区切り値 (CSV) ファイルに、見込顧客を現金データにエクスポートします。 次のエンティティからデータをエクスポートします。

    - [口座](#account-table)
    - [連絡](#contact-table)
    - [請求書](#invoice-table)
    - 製品の請求
    - [注文](#order-table)
    - [受注製品](#order-products-table)
    - [製品](#products-table)
    - [見積](#quote-and-quote-product-tables)
    - [見積製品](#quote-and-quote-product-tables)

3. 販売環境から見込顧客から入金ソリューションをアンインストールします。 この手順により、見込顧客からの入金ソリューションの列と対応するデータが削除されます。
4. 二重書き込みソリューションをインストールします。
5. 1 つ以上の法人に対して、Finance and Operations アプリと Customer Engagement アプリの間に二重書き込み接続を作成します。
6. デュアル書き込みテーブル マップを有効にし、必要な参照データに対して初期同期を実行します。 (詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) をご覧ください。) 必須データの例として、顧客グループ、支払条件、支払スケジュールがあります。 初期化が必要なテーブル (勘定、見積、見積行、注文、注文など) に対して二重書き込みマップを有効にすることはできません。
7. Customer Engagement アプリで、**詳細設定 \> システム設定 \> データ管理 \> 複製検出ルール** に移動し、すべてのルールを無効にします。
8. 手順 2 に示したテーブルを初期化します。 手順については、このトピックの残りのセクションを参照してください。
9. Finance and Operations アプリを開き、テーブル マップ (勘定、見積、見積依頼行、注文、注文の行テーブル マップなど) を有効にします。 その後初期同期を実行します。 (詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) を参照してください。) このプロセスでは、Finance and Operations 処理ステータス、出荷先住所と請求先住所、サイト、倉庫などの追加情報をアプリケーションから同期します。

## <a name="account-table"></a>アカウント テーブル

1. **会社** 列に、**USIM** などの会社名を入力します。
2. **関係タイプ** 列に、**顧客** を静的値として入力します。 すべての勘定レコードをビジネス ロジックで顧客として分類する場合はそうではありません。
3. **顧客グループ ID** 列に、Finance and Operations アプリの顧客グループ番号を入力します。 見込顧客からの入金ソリューションの既定値は **10** です。
4. **勘定番号** をカスタマイズせずに見込顧客から入金ソリューションを使用している場合は、**当事者番号** 列に **勘定番号** の値を入力します。 カスタマイズが存在し、当事者番号が分からない場合は、この情報を Finance and Operations アプリから取り込む必要があります。

## <a name="contact-table"></a>連絡先テーブル

1. **会社** 列に、**USIM** などの会社名を入力します。
2. CSV ファイルの **IsActiveCustomer** 値に基づいて、次の列を設定します。

    - CSV ファイルで **IsActiveCustomer** が **はい** に設定されている場合は、**販売可能** 列を **はい** に設定します。 **顧客グループ ID** 列に、Finance and Operations アプリの顧客グループ番号を入力します。 見込顧客からの入金ソリューションの既定値は **10** です。
    - **ISActiveCustomer** が CSV ファイルで **"いいえ**" に設定されている場合は、**販売可能** 列を **"いいえ"** に設定し、**連絡先対象** を **顧客** に設定します 。

3. **連絡先番号** をカスタマイズせずに見込顧客を現金化ソリューションを使用している場合は、次の列を設定します。

    - 連絡先番号を CSV ファイル (**msdynce\_contactnumber**) から **連絡先** テーブルの連絡先 (**msdyn\_contactnumber**) に移行します。
    - **当事者番号** 列の **連絡先番号** テーブルの値を使用します。
    - **アカウント番号/当事者番号 ID** 列の **連絡先番号** テーブルの値を使用します。

## <a name="invoice-table"></a>請求テーブル

**請求書** テーブルのデータは、Finance and Operations アプリから Customer Engagement アプリに対して一方向に流れる設計なので、初期化の後で初期化を行う必要はありません。 初期同期を実行して、必要なすべてのデータを Finance and Operations アプリから Customer Engagement アプリに移行します。 詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) を参照してください。

## <a name="order-table"></a>オーダー テーブル

1. **会社** 列に、**USIM** などの会社名を入力します。
2. CSV ファイル内の **オーダー ID** 列の値を **販売注文番号** 列にコピーします。
3. CSV ファイル内の **顧客** 列の値を **販売注文番号** 列にコピーします。
4. CSV ファイルの **国/地域に出荷** 列の値を **国/地域に出荷** 列にコピーします。 この値の例として、**US** と **United States** があります。
5. **入荷希望日** 列を設定します。 入荷日を使用しない場合は、CSVファイル内の **配送指定日** 列、**履行日** 列、**提出日** 列を使用します。 この値の例は **2020-03-27T00:00:00Z** です。
6. **言語** 列を設定します。 この値の例は **en-us** です。
7. **品目ベース** 列を使用して **オーダー タイプ** 列を設定します。

## <a name="order-products-table"></a>オーダー製品テーブル

- **会社** 列に、**USIM** などの会社名を入力します。

## <a name="products-table"></a>製品テーブル

**製品** テーブルのデータは、Finance and Operations アプリから Customer Engagement アプリに対して一方向に流れる設計なので、初期化の後で初期化を行う必要はありません。 初期同期を実行して、必要なすべてのデータを Finance and Operations アプリから Customer Engagement アプリに移行します。 詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) を参照してください。

## <a name="quote-and-quote-product-tables"></a>見積および見積製品テーブル

**見積** テーブルについては、このトピックの前にある [オーダー テーブル](#order-table) セクションの指示に従ってください。 **見積製品** テーブルについては、[オーダー製品テーブル](#order-products-table) セクションの指示に従ってください。
