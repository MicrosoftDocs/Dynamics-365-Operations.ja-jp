---
title: 拡張ログオン機能の設定と使用
description: この記事では、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリケーションの拡張ログオン機能の設定方法および使用方法について説明します。
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e27e8d94adccc46559089928b0481442306567ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884314"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>拡張ログオン機能の設定と使用

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリケーションの拡張ログオン機能の設定方法および使用方法について説明します。

クラウド POS (CPOS) および Modern POS (MPOS) は、小売店舗の従業員が、磁気ストライプ リーダー (MSR) を使用してバーコードをスキャンしたり、カードをスワイプして POS アプリケーションにログインできる、拡張ログオン機能を提供します。

## <a name="set-up-extended-logon"></a>拡張ログオンの設定

小売店舗でPOS レジスターの拡張ログオンを設定するには、次の手順を実行します。

1. Commerce Headquarters で、**Retail と Commerce \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。 
2. 左ナビゲーション ウィンドウで、小売店舗に関連付けられている機能プロファイルを選択します。
3. **機能** FastTab の **追加のログオン認証オプション** で、必要に応じて次のオプションを **はい** または **いいえ** に設定します。

    - **スタッフ バーコード ログオン** – 従業員がバーコードをスキャンして POS にサインインするようにするには、このオプションを **はい** に設定します。 
    - **スタッフ バーコード ログオンにパスワードが必要** – 従業員がバーコードをスキャンして POS にサインインする時にパスワードを入力するようにするには、このオプションを **はい** に設定します。
    - **スタッフ カード ログオン** – 従業員がカードをスワイプして POS にサインインするようにするには、このオプションを **はい** に設定します。
    - **スタッフ カード ログオンにパスワードが必要** – 従業員がカードをスワイプして POS にサインインする時にパスワードを入力するようにするには、このオプションを **はい** に設定します。

バーコードまたはカードは、従業員に割り当て可能な資格情報に関連付けられています。 資格情報には 6 文字以上必要です。 最初の 5 文字を含む文字列は一意である必要があり、従業員の検索に使用される *資格情報 ID* と見なされます。 残りの文字はセキュリティの確認に使用されます。 たとえば、2 つのカードがあり、そのうち 1 つは資格情報 12345DGYDEYTDW、もう 1 つは資格情報 12345EWUTBDAJH であるとします。 この 2 つのカードには同じ資格情報 ID 12345 があるため、両方を従業員に正しく割り当てることはできません。

## <a name="assign-extended-logon"></a>拡張ログオンの割り当て

既定では、マネージャのみが作業者に拡張ログオンを割り当てることができます。 拡張ログオンを割り当てるには、POS で **拡張ログオン** に移動します。 検索フィールドに、作業者 ID を入力して、作業者を検索します。 作業者を選択し、**割り当て** をクリックします。 次のページで、作業者に割り当てる拡張ログオンを機械に通すかスキャンします。 読み取りまたはスキャンが正常に読み取られた場合、**OK** ボタンが使用できるようになります。 その作業者の拡張ログオンを保存する場合、**OK** をクリックします。

## <a name="delete-extended-logon"></a>拡張ログオンの削除

作業者に割り当てられている拡張ログオンを削除するには、**拡張ログオン** 操作にて作業者を検索します。 作業者を選択し、**割り当て解除** をクリックします。 その作業者と関連付けられるすべての拡張ログオン資格情報が削除されます。

## <a name="use-extended-logon"></a>拡張ログオンの使用

拡張ログオンが構成され、従業員にバーコードまたは磁気ストライプが割り当てられると、従業員は POS ログオン ページが表示されている間に、自分のカードをスワイプするかスキャンするだけで済みます。 ログオンを続行するためにパスワードも必要な場合、従業員は自分のパスワードの入力を求められます。

## <a name="extend-extended-logon"></a>拡張ログオンの拡張

拡張ログオン機能をあらかじめ実装するには、資格情報の長さが 6 文字以上で、最初の 5 文字 (資格情報 ID) が一意である必要があります。 元々は、開発者が特定の実装の要件に合わせてカスタマイズできるサンプルとして意図されていました。 (たとえば、より多くの文字をサポートしたり、異なるセキュリティ確認ルールを使用したりするようにカスタマイズすることができます。) 拡張ログオンの拡張機能を作成する方法の詳細については、[MPOS および Cloud POS の拡張ログオン機能を拡張する](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/) を参照してください。

ログオン サービスは、パーム スキャナーなどの追加ログオン デバイスをサポートするように拡張することもできます。 詳細については、[POS 拡張ドキュメント](dev-itpro/pos-extension/pos-extension-overview.md) を参照してください。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
