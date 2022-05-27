---
title: 廃棄コードを設定します
description: 顧客が返品した品目のプロセス方法を指定する廃棄コードを設定できます。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8579190082d35424a5a87f6b5e2b34a79db71014
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670023"
---
# <a name="set-up-disposition-codes"></a>廃棄コードを設定します 

[!include [banner](../includes/banner.md)]


顧客が返品した品目のプロセス方法を指定する廃棄コードを設定できます。 たとえば、返品品目が修理されてから顧客に返送されることを示す **Repair and return** という名前の廃棄コードを作成します。 顧客が返品した品目に通常使用される廃棄コードの例については、[返品品目の廃棄方法の指定](specify-how-to-dispose-of-returned-items.md)を参照してください。

品目が返品された理由を説明するのに役立つ理由コードも設定できます。 理由コードの詳細については、[返品理由コードの設定](set-up-return-reason-code.md)を参照してください。

1.  **販売とマーケティング** \> **設定** \> **販売注文** \> **返品** \> **廃棄コード** に移動します。

2.  **新規作成** を選択して、新しい廃棄コードを作成します。

3.  廃棄コードの内容を示す一意の名前を入力し、アクションを選択して、説明を入力します。

4.  この廃棄コードに顧客請求金額を関連付ける場合は、**雑費** ボタンを選択して **雑費の設定** フォームを開きます。

5.  会社独自の廃棄コードに対応する外部コードを定義する場合は、**外部コード** ボタンを選択して **外部コード** フォームを開きます。

## <a name="see-also"></a>参照

[顧客からの返品の概要](disposition-and-return-reason-codes.md)

[廃棄コード (フォーム)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[自動請求 (フォーム)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))

[外部コード (フォーム)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]