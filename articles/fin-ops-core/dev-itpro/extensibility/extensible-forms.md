---
title: 拡張可能フォームの書き込み
description: この記事では、拡張可能フォームを書き込む方法について説明します。
author: smithanataraj
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.custom: 268724
ms.assetid: ''
ms.openlocfilehash: 11ac4ce97ec7da68787d0c8998780e14f9ecc015
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270843"
---
# <a name="write-extensible-forms"></a>拡張可能フォームの書き込み

[!include [banner](../includes/banner.md)]

## <a name="methods-on-forms"></a>フォーム上のメソッド
+ 一般に、拡張可能なメソッドを記述するためのガイドラインは、フォーム メソッドにも適用されます。
+ コマンド チェーン (CoC) は、フォームの非プライベート メンバー (クラスの非プライベート メンバーと同じ) にアクセスを許可します。
+ CoC は入れ子になったクラスで有効になります。 そのため、フォーム上のさまざまなレベルで定義されているメソッドは拡張可能です。

> [!NOTE]
> フォームのメソッドの 1 つの制限として、データ ソース メソッドの場合、カーネルで定義されているメソッドのみで拡張が有効になります。つまり、フォーム データ ソースで定義されたメソッドは拡張可能ではありません。 これは今後のプラットフォーム更新で使用できます。

## <a name="field-groups"></a>フィールド グループ
可能であれば必ずフィールド グループの使用を検討してください。 これにより、独立系ソフトウェア ベンダー (ISV) はフィールド グループを拡張するときにそのフィールドを無料で追加できます。

## <a name="form-controls"></a>フォーム コントロール
コントロールが移動により拡張不可になった場合、フォーム コントロールでの移動により中断が発生する可能性があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
