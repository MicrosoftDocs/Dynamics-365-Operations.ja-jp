---
title: 注文を終了しようとする場合の合計良品数量のエラー
description: 製造オーダーを終了して完了報告をしようとしている場合、良品数量の合計のエラーが表示される場合があります。 このページでは、その理由と問題を修正する方法について説明します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476866"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>製造オーダーを終了しようとする場合の合計良品数量のエラー

## <a name="symptoms"></a>現象

レポートを完了仕訳帳として製造オーダーに転記しようとすると、次のエラー メッセージが表示されます。

> 生産完了が報告された良品数量の合計が %1 になります。 最後の工程に対するフィードバックは合計で 0.00 です。

## <a name="cause"></a>原因

この問題は、前回の工程で転記された数量が正しくなかった場合に発生します。 たとえば、生産が開始されているが、開始する必要のある数量が割り当てられていない場合、工順カード仕訳帳は明細行なしで転記されます。 状況を確認するには、製造オーダーを開き、アクション ウィンドウの **表示** タブで、**工順カード** を選択します。

## <a name="resolution"></a>解決策

仕訳帳が正しく転記されなかった工程に対して追加の仕訳帳を転記することにより、この問題を解決できます。 製造オーダーを再開し、追加の仕訳帳を転記する場合に選択します。 このアクションでは製造オーダーは開始されませんが、仕訳帳は転記されます。 その後、工順カードに転記済の数量が表示され、製造オーダーを正常に終了することができます。
