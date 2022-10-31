---
title: 状態が空白の小切手の作成
description: この記事では、銀行口座に対して空白の小切手を作成する方法について説明します。
author: angelad116
ms.date: 10/24/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 151991b399a30087c484262706e414e4e294bf7f
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715428"
---
# <a name="create-checks-that-have-blank-status"></a>状態が空白の小切手の作成

[!include [banner](../includes/banner.md)]

この記事では、空白の小切手を作成する方法について説明します。 たとえば、破損した小切手を記録して支払いに使用できない場合は、その小切手を空白で作成することができます。

**小切手** ページでは、小切手に対してメンテナンス タスクを実行します。 たとえば、新しい小切手番号を作成したり、小切手を削除したりすることができます。 また、状態が **空白** の小切手を作成することもできます。 空白の小切手が作成された後は、システムで削除または再利用することはできません。

> [!NOTE]
> この機能は、**機能管理** ページの **小切手ページで状態が空白の小切手を作成する** 機能をオンにしている場合にのみ、**小切手** ページで使用できます。 この機能が有効になっていない場合、状態が **空白** である小切手は、買掛金勘定の支払生成プロセス中に、**小切手による支払** ダイアログ ボックスからのみ作成できます。

**小切手** ページを開くには、**現金および銀行管理 \> 銀行口座 \> 銀行口座** に移動し、アクション ペイン、**支払の管理** タブ、**関連情報** グループで、**小切手** を選択します。 または、**現金および銀行管理 \> 照会およびレポート \> 小切手** に移動します。

状態が **空白** の小切手を作成するには、アクション ペインで **空白の小切手の作成** を選択します。 システムが空白の小切手を作成している間、関連付けられている銀行口座が一時的に無効化されます。 この動作により、空白の小切手が作成されたときと同時に、支払が生成されるリスクが低下します。 処理が完了すると、関連付けられている銀行口座が再度有効化されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
