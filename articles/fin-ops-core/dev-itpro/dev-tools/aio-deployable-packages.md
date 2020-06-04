---
title: オールインワン配置可能パッケージ
description: このトピックでは、オールインワンの配置可能なパッケージの概念とその使用方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 969b76d03a123259c3a1ff95fd44b975d17769e4
ms.sourcegitcommit: 78a1aa37f9a1565135b139e36501b759e7b2f849
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2020
ms.locfileid: "3374785"
---
# <a name="all-in-one-deployable-packages"></a>オールインワン配置可能パッケージ

お客様は、ソフトウェア配置可能パッケージを適用することにより、各自の環境内のソフトウェアを更新できます。 これらのパッケージは、お客様自身がカスタマイズの形で作成できます。 また、パートナーや独立系ソフトウェア ベンダー (ISV) によって提供されることもあります。 Microsoft では、これらのさまざまなパッケージを 1 つのパッケージにまとめてから、環境に適用することをお勧めします。 セルフサービス環境をお持ちのお客様にとって、このアプローチは難しい要件です。

このトピックでは、オールインワン配備可能パッケージを作成および管理するためのベスト プラクティスについて説明します。

> [!IMPORTANT]
> - オールインワン配置可能パッケージでは **ない** 配置可能パッケージのサポートは、2020 年 10 月 31 日に終了します。
> - 現在、支払コネクタが環境に配置されている場合、[支払コネクタ パッケージを作成](../../../commerce/dev-itpro/payment-connector-package.md) して、オールインワン配置可能パッケージに含める必要があります。
> - 現在、小売販売時点管理で Microsoft Dynamics 365 Commerce 機能を使用している場合は、[セルフサービス インストーラーを同期](../../../commerce/dev-itpro/Synchronize-installers.md) する必要もあります。

## <a name="what-is-an-all-in-one-deployable-package"></a>オールインワン配置可能パッケージとは何ですか?

オールインワン配置可能パッケージは、現在環境内にあるすべてのモデルとバイナリを含むソフトウェア配置可能パッケージです。 これは、環境内の Microsoft 以外のすべてのソフトウェアを表す単一のパッケージと考えてください。

たとえば、**SandboxTest** と **SandboxPreProd** という 2 つの環境があるとします。

<img src="media/AIO_PKG.png" width="500px" alt="All-in-one deployable package comparison" />

ソフトウェア配置可能パッケージに CustomizationA、CustomizationB、ISV1 が含まれている場合、それは SandboxTest 環境用の完全に配置可能なパッケージです。 これは、モデルの一覧と完全に一致するためです。 また、インストールされているすべてのモデルに加えて CustomizationB が含まれているため、SandboxPreProd 環境用の完全に配置可能なパッケージでもあります。

ただし、ソフトウェア配置可能パッケージに CustomizationA のみが含まれている場合は、どちらの環境にも完全に配置できません。 パッケージには、既にインストールされている一部のモデルが含まれていません。

## <a name="how-do-i-create-an-all-in-one-deployable-package"></a>オールインワン配備可能パッケージをどのように作成しますか?

オールインワン配置可能パッケージを作成するには、主に次の 2 つの方法があります。

- 継続的インテグレーション/継続的配置モデルを使用している場合は、既にオールインワン配置可能パッケージを作成しています。
- ビルド環境がない場合は、Microsoft Visual Studio でパッケージを作成することができます。 詳細については、[配置可能パッケージの作成](../deployment/create-apply-deployable-package.md)を参照してください。

## <a name="what-if-my-isv-packages-dont-contain-source-code"></a>ISV パッケージにソース コードが含まれていない場合どうなりますか?

ISV はソース コードを共有するかどうかを選択できます。 共有しない場合は、バイナリのみのパッケージを提供します。 このパッケージは、オールインワン配置可能パッケージで簡単に管理できます。 手順については、[ソース コントロールを使用してサード パーティ モデルとランタイム パッケージを管理](manage-runtime-packages.md) を参照してください。

## <a name="why-are-these-packages-important"></a>これらのパッケージはなぜ重要なのですか?

完全に配置可能なパッケージを使用するベスト プラクティスは、特定の環境に適用されるパッケージの複雑さと数を減らすのに役立ちます。 場合によっては、異なるパッケージをインストールすると、環境の動作が変わることがあります。 たとえば、ModelB の後に ModelA をインストールするのではなく、ModelA の後に ModelB をインストールするとします。

さらに、このアプローチはセルフサービス環境にとって、難しい要件です。 これは、これらの環境ではコンテナー詰めテクノロジを使用して、パッケージを適用するたびに、新しい環境を構築するためです。 今日 ModelA を適用し、明日 ModelB のみを適用すると、ModelA を効果的にアンインストールできます。
