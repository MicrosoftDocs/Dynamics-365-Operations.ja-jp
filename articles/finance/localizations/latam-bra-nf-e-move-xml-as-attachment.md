---
title: NF-e XML ファイルを添付として移動する
description: このトピックでは、Microsoft Dynamics 365 Finance または Dynamics 365 Supply Chain Management データベースから NF-e XML ファイルを移動し、添付ファイルとして使用する方法について説明します。
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c7b82d486cecf6b20f1283fa609c360b3003efca
ms.sourcegitcommit: ebf6546835e4d6a80aea1dfae81e119e294387f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799449"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>NF-e XML ファイルを添付として移動する

[!include [banner](../includes/banner.md)] 


電子会計ドキュメント (NF-e) が発行されると、XML ファイルが作成され、Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management データベースに格納 されます。 ブラジルのローカライズでは、**NF-e XML ファイルを添付として移動する** 機能を使用して、それらの XML ファイルが使用しているデータベース容量を解放できます。

特定の日付範囲および会計施設の場合、この機能は、Finance または Supply Chain Management データベースから Azure サブスクリプションの Blob Storage に NF-e XML ファイルを移動します。 この移動により、ファイルは添付ファイルとしてのみ使用できるようになります。 XML ファイルが正常に Blob Storage に移動されると、元のファイルが Finance または Supply Chain Management データベースから削除されます。 そのため、使用されるファイルのデータベース容量が解放されます。

**NF-e XML を添付として移動する** 機能を有効にするには、以下の手順に従います。

1. Finance または Supply Chain Management で、**機能管理** ワークスペースを開きます。
2. **すべて** タブで、**NF-e XML を添付として移動する** 機能を探して選択します。
3. **直ちに有効化** を選択します。

次の手順に従って、NF-e XML ファイルを添付として移動します。

1. **売掛金勘定** \> **会計ドキュメント** \> **電子会計ドキュメント** \> **NF-e XML を添付として移動する** の順に移動します。
2. **開始日** および **終了日** フィールドで開始日と終了日を選択します。
3. **会計施設 ID** フィールドで値を選択します。
4.  **OK** を選択します。

> [!IMPORTANT]
> このプロセスは、元に戻すことはできません。 NF-e XML ファイルを移動した後、**会計ドキュメント** ページの上部で **添付ファイル** を選択した場合のみユーザーはファイルを表示できます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
