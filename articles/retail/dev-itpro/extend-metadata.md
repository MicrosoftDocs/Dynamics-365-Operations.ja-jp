---
title: 既定の Retail Server メタデータ コントローラーの拡張
description: この記事では、CommerceModelFactory クラスを拡張するコードを説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 31641
ms.assetid: 6e25b63e-be1e-42fc-b1bd-c91585cd624d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ceac528e461ace2448e0ab4b52fc49b85144baf7
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023470"
---
# <a name="extend-the-default-retail-server-metadata-controller"></a>既定の Retail Server メタデータ コントローラーの拡張

[!include [banner](../includes/banner.md)]

この記事では、CommerceModelFactory クラスを拡張するコードを説明します。

OData を Microsoft Dynamics 365 Retail と共に使用するとき、メタデータはクライアントとサーバー間の契約を定義します。 メタデータ はエンティティ定義とアクション定義を公開しているため、サーバー側で変更を加えると、クライアント側のツールを使用してプロキシ コードを生成できます。 したがって、メンテナンスにかかる開発者の労力が軽減されます。 新規または変更されたエンティティおよびアクションを使用するには、メタデータを拡張する必要があります。 Retail サーバーには、**CommerceModelFactory** という既定メタデータ コントローラーがあります。 既定のコント ローラーを拡張するには、**エクスポート** 属性と **IEdmModelFactory** インターフェイスを使用する新しいクラスを作成します。 既存のコードを追加してオーバーライドすることができます。 たとえば、新しいエンティティ セット、新しいアクション、新しい複合型、または新しい例外タイプを追加することができます。 次の例では、**ExtendedEdmModelFactory** クラスは **CommerceModelFactory** メタデータ コントローラーを拡張して、**NewAction** という新しいアクションおよび **NewEntities** という新しいエンティティ セットを作成します。 サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。

    namespace Microsoft.Dynamics.RetailServer.Samples.Extensions
    {
        using System.ComponentModel.Composition;
        using Microsoft.Dynamics.Retail.StoreServerServiceLibrary;
        [Export(typeof(IEdmModelFactory))]
        public class ExtendedEdmModelFactory : CommerceModelFactory
        {
            protected override void BuildNonBindableActions()
            {
                base.BuildNonBindableActions();
                var NewAction = BindAction("NewAction");
                NewAction.Returns<string>();
            }
            protected override void BuildEntitySets()
            {
                base.BuildEntitySets();
                BuildEntitySet<NewEntity>("NewEntities");
            }
        }
    }



