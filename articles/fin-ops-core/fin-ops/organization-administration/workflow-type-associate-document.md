---
title: ワークフロー ドキュメント クラスをワークフロー タイプと関連付ける
description: このトピックでは、ワークフロー タイプにワークフロー ドキュメント クラスを関連付ける方法について説明します。
author: RobinARH
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 47d685183e1117f4c31665de0fcdb928140c92c4
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783118"
---
# <a name="associate-a-workflow-document-class-with-a-workflow-type"></a>ワークフロー ドキュメント クラスとワークフロー タイプの関連付け 

[!include [banner](../includes/banner.md)]

ワークフローを作成するには、ワークフロー ドキュメント クラスをワークフロー タイプにバインドする必要があります。 ワークフロー ドキュメント クラスには、ワークフローが使用するテーブル データ フィールドへの参照が含まれています。 このトピックでは、ワークフロー タイプにワークフロー ドキュメント クラスをバインドする方法について説明します。

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