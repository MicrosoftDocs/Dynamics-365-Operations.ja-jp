---
title: ワークフロー ドキュメント クラスとワークフロー タイプの関連付け
description: この記事では、ワークフロー タイプにワークフロー ドキュメント クラスを関連付ける方法について説明します。
author: josaw1
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.openlocfilehash: 968ae8b4b3bc2285540dcc0a17a89a5afd96717f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287060"
---
# <a name="associate-a-workflow-document-class-with-a-workflow-type"></a>ワークフロー ドキュメント クラスとワークフロー タイプの関連付け 

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

ワークフローを作成するには、ワークフロー ドキュメント クラスをワークフロー タイプにバインドする必要があります。 ワークフロー ドキュメント クラスには、ワークフローが使用するテーブル データ フィールドへの参照が含まれています。 この記事では、ワークフロー タイプにワークフロー ドキュメント クラスをバインドする方法について説明します。

> [!NOTE]
> **ワークフロー** ウィザードを使用してワークフロー タイプを作成した場合は、ワークフロー ドキュメント クラスをワークフロー タイプに既にバインドしています。

次の手順を開始する前に、コンフィギュレーション ユーザー インターフェイス (UI) の条件に使用されるテーブル フィールドを公開するためのワークフロー ドキュメント クラスを作成する必要があります。 詳細については、 [新しいワークフロー ドキュメント クラスの作成](workflow-type-document-create.md) を参照してください。

## <a name="bind-a-workflow-document-class-to-a-workflow-type"></a>ワークフロー ドキュメント クラスをワークフロー タイプにバインドする

1. アプリケーション エクスプローラーで、 **ワークフロー** ノードを展開します。
2. **ワークフロー タイプ** ノードで、ワークフロー ドキュメント クラスをバインドするワークフロー タイプを右クリックし、 **プロパティ** を選択します。
3. **プロパティ** シートで、 **ドキュメント** プロパティをワークフロー ドキュメントを定義するワークフロー ドキュメント クラスに設定します。

## <a name="see-also"></a>参照

[新しいワークフロー タイプの作成](workflow-type-create-new.md)

[ワークフロー ドキュメント クラスの作成](workflow-type-document-create.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
