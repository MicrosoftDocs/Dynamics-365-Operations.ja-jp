---
title: 資産と作業指示書
description: このトピックでは、資産管理の資産と作業指示書について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b56234eac247185c5cd4d8ab45a65d258013acd
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571372"
---
# <a name="assets-and-work-orders"></a>資産と作業指示書

[!include [banner](../../includes/banner.md)]

 

このトピックでは、資産管理の資産と作業指示書について説明します。 資産と作業指示書は、資産管理の中心的な部分です。 *資産*は、継続的なメンテナンスとサービスを必要とする機械または機械部品です。 資産は、階層構造で作成でき、機能の場所に関連付けることができます。 メンテナンス ジョブは、資産構造のすべてのレベルで計画できます。

製品情報や資産仕様、必要なメンテナンス計画など、さまざまなデータが資産ごとに設定されます。 次の図は、資産データの概要と、資産のジョブ タイプへの関連付けを示しています。 赤色のテキストは、継承と依存関係を示す場合などに使用されます。

![ジョブ タイプに関連する資産データを示す図](media/05-overview-image.png)

すべての作業指示書には、予防的メンテナンス、修繕メンテナンス、検査などの作業指示書タイプがあります。 作業指示書には、1 つ以上のワーク オーダー ジョブが含まれています。 すべての作業指示書ジョブは、資産および関連するジョブ タイプに対して実行する必要があるジョブを定義します。 関連するジョブ タイプの例には、10,000 km、50,000 km、1 年間のオーバーホール、および安全検査が含まれます。 1 つの作業指示書を複数の資産に関連付けることができます。

次の図は、作業指示書のキー データの概要を示します。

![作業指示書のキー データを示す図](media/06-overview-image.png)

作業指示書は別の作業指示書に関連付けることができ、ジョブ タイプには作業指示書を作成する後続のジョブを含めることができます。 一般に、作業指示書間に依存関係はありません。 したがって、作業指示書のライフサイクル状態を変更でき、各々無関係にスケジューリングできます。

作業指示書は、修繕メンテナンス、予防的メンテナンス、または再有効化メンテナンスに関連するさまざまな方法で作成できます。 また、作業指示書を手動で作成することもできます。 次の図は、作業指示書の自動または手動で作成するプロセスの概要を示します。

![作業指示書の自動または手動作成を示す図](media/07-overview-image.png)

作業指示書でメンテナンス ジョブをスケジュールして実行する場合、複数のステップを完了しておく必要があります。 次の図は、作業指示書処理の概要を示します。

![作業指示書の処理の概要を示す図](media/08-overview-image.png)

> [!NOTE]
> 一般に、Dynamics 365 Supply Chain Management および**アセット管理**モジュールで作業する場合は、**新規**を選択して新しいレコードを作成するか、**編集**を選択して既存のレコードを更新してから、**保存**を選択して新規または編集したデータを保存します。
