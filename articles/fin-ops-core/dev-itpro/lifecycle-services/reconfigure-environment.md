---
title: 新しいプラットフォームまたはトポロジを使用するために環境を再構成
description: この記事では、新しいプラットフォームまたはトポロジを使用して環境を再構成する方法と、既存の環境の構成を更新する方法について説明します。
author: PeterRFriis
ms.date: 12/05/2017
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2017-12-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 35a2094fb90b19b3c9fadae19d543441522afea7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866374"
---
# <a name="reconfigure-environments-to-take-a-new-platform-or-topology"></a>新しいプラットフォームまたはトポロジを使用するために環境を再構成

[!include [banner](../includes/banner.md)]

この記事では、新しいプラットフォームまたはトポロジを使用して環境を再構成する方法と、既存の環境の構成を更新する方法について説明します。  

## <a name="prerequisites"></a>必要条件
この記事の手順を実行する前に、ローカル エージェントを更新する必要があります。 詳細については、記事の、[ローカル エージェントの更新](update-local-agent.md) を参照してください。 この記事にある手順は、バージョン 1.1.0 以上のローカル エージェントでのみ動作します。 

## <a name="reconfigure-your-environment"></a>環境の再構成

1. Lifecycle Services (LCS) で、オンプレミスのプロジェクトに移動し、**環境** ブレードを開きます。 

2. 新しい配置を再設定するかどうかに基づいて、次のいずれかを実行します。

- 環境を再構成する場合は、**再構成** をクリックします。
- 新しい展開またはトポロジーを使用する必要がある場合は、使用しているプラットフォーム用の新しいトポロジーを選択し、環境名を入力します。 同じ名前を使用したり、新しい名前を入力することができます。 
  
3. **詳細設定** をクリックし、コンフィギュレーションを更新します。 以前の展開の設定が保存されます。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
