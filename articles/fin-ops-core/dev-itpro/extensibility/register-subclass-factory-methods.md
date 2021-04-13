---
title: ファクトリ メソッドのサブクラスを登録
description: このトピックでは、独自のバリエーションを工場に登録する方法について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: a8844c5135916f5c327e5bf0f446ef9fc2165a13
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744531"
---
# <a name="register-subclasses-for-factory-methods"></a>ファクトリ メソッドのサブクラスを登録

[!include [banner](../includes/banner.md)]

クラス継承は、他のオブジェクト指向言語と同様に、X++ の中心的概念です。 オブジェクト指向戦略パターンは、X++ ビジネス ロジック全体で使用されます。 このパターンでは、動作のバリエーションをサブクラスでカプセル化することができ、業務プロセスが抽象基本クラスまたはインターフェイスを使用します。 ファクトリ メソッドは、特定のサブクラスのインスタンスを作成することによって、使用されるバリエーションを決定します。

このトピックでは、独自のバリエーションを工場に登録する方法について説明します。

X++ では、ファクトリはリフレクションを使用して、次のタスクを実行します。

+ 正しいサブクラスを検索します。 ファクトリは、拡張フレームワークを使用して、階層内のすべてのサブクラスで特定の属性セットを検索します。 サブクラスを修飾する属性がファクトリに渡されたパラメータと一致する場合、その特定のクラスが使用されます。
+ インスタンスを作成します。 正しいタイプが識別された後、リフレクションを使用してクラスのインスタンスを作成します。

次の図は、一般的な装飾階層を示しています。

![各サブクラスが属性で装飾されている、3 つのサブクラスを持つクラス階層](media/hierarchy.png)

X++ では、2 つの拡張フレームワークは同じ目的で機能します。 ファクトリ メソッドの実装担当者は、使用する拡張フレームワークを決定します。

+ [SysExtension](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/sysextension-framework-to-the-rescue)

  - この拡張フレームワークは、利用しやすくするためにカスタム属性を使用します。
  - 同じインスタンスが繰り返し作成されるときに、パフォーマンスを多少節約する単一をサポートします。 この拡張フレームワークは、ステートレスなサブクラスに特に便利です。
  - バリアントを決定するために頻繁に使用される拡張可能な列挙をシームレスにサポートしています。

+ SysPlugin

  - この拡張フレームワークは、Managed Extension Framework に基づいています。 マネージ拡張フレームワークは、SysPlugin 拡張フレームワークを非 X++ コードで使用できるようにします。
  - **ExportMetadataAttribute** 属性を使用してバリアントを修飾し、文字列ベースとなります。
  - **ExportAttribute** 属性を使用してバリアントを見つけやすくします。

## <a name="introduce-a-new-variant"></a>新しいバリアントの導入

1. 実装する必要があるバリアントの基本クラス (またはインタフェース) を特定します。
2. 基本クラスの新しいサブクラスを作成し、バリエーションを実装します。
3. クラスを登録するために必要となる属性を識別します。 次の 2 つのアプローチがあります。

    + 階層内のその他のサブクラスで定義されている属性を検索します。
    + ファクトリ メソッドの実装を確認します。 その実装には、ファクトリ メソッドが検索する属性が含まれます。

4. バリエーションに一致するために使用された属性でサブクラスを修飾します。

## <a name="sysextension-example"></a>SysExtension 例

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::About)]
class WHSWorkExecuteDisplayAbout extends WHSWorkExecuteDisplay
{
    // Your code here.
}
```

## <a name="sysplugin-example"></a>SysPlugin 例

```xpp
[ExportMetadataAttribute('CaseIAssociation', 'Lead'),
ExportAttribute('Dynamics.AX.Application.CaseIAssociation')]
class smmLeadCaseAssociationProvider implements CaseIAssociation
{
    // Your code here.
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]