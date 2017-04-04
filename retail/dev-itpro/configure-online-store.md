---
title: "オンライン ストアのコンフィギュレーション"
description: "この記事では、Microsoft Dynamics 365のオンライン店舗を設定および管理&quot;を中央からヘルプ トピックへのリンクが提供されます。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: 4da710b57d03621fdf9abbf5a9598859e1e9aafd
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-online-store"></a>オンライン ストアのコンフィギュレーション

この記事では、Microsoft Dynamics 365のオンライン店舗を設定および管理"を中央からヘルプ トピックへのリンクが提供されます。

次の表のヘルプ トピックに記載されている工程- Retailのコンポーネントおよび工程のクライアントのDynamics 365 for Retailのオンライン店舗365 for Operationsを設定します。

## <a name="configure-an-online-store"></a>オンライン ストアのコンフィギュレーション
| タスク                                                | 細目                                                                                                                                                                                                                                                                                                                                                   | トピック                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Retailのコンポーネントをコンフィギュレーションします。                        | 小売操作の情報を設定および管理します。 この情報には、店舗、税、製品、ギフト カード、プロモーション、割引が含まれます。                                                                                                                                                                                                          | [の設定と管理、] (https://technet.microsoft.com/en-us/library/hh597201.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)                                                                                                                                                                                                                                                                                           |
| 小売チャンネルのナビゲーション階層を設定します。    | オンライン ストアを通じて提供する製品のカテゴリ構造を設定するために、小売チャンネル ナビゲーション カテゴリ階層を作成します。 カテゴリ階層を定義したり、カテゴリ、製品、製品の属性グループと属性値が割り当てられます。 オンライン店舗に、カテゴリ階層を割り当てます。                            | [小売階層]設定 (https://technet.microsoft.com/en-us/library/hh580593.aspx) (Microsoft Dynamics AX 2012のTechNetの内容) [設定]、[属性の型] (https://technet.microsoft.com/en-us/library/hh227548.aspx) (Microsoft Dynamics AX 2012) [設定]の属性グループ] (https://technet.microsoft.com/en-us/library/jj728713.aspx) (Microsoft Dynamics AX 2012のTechNetの内容) のTechNetの内容 |
| 組織階層にオンライン店舗を追加します。 | 製品品揃えを割り当てるか、または作成した、または生成され、オンライン店舗からの情報を含むレポートができるオンライン店舗の注文を行う前に、一つまたは複数の組織階層に店舗を割り当てる必要があります。 少なくとも、オンライン ストアを製品の品揃えを含む組織階層に割り当てる必要があります。 | [設定オンライン店舗] (https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)                                                                                                                                                                                                                                                                                                      |
| オンライン店舗の荷渡方法を追加します。          | その配送方法をオンライン店舗のサービス選択します。                                                                                                                                                                                                                                                                                                 | [設定オンライン店舗] (https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)                                                                                                                                                                                                                                                                                                      |
| 属性のマッピングおよびメタデータを追加します。                   | 各カテゴリまたはチャンネルの製品の属性をMicrosoft SharePointサイトのオンライン店舗に実行するかを選択します。                                                                                                                                                                                              | [設定オンライン店舗] (https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)                                                                                                                                                                                                                                                                                                      |

## <a name="configure-online-store-products"></a>オンライン店舗の製品を設定します。
| タスク                                 | 細目                                                                                                                                           | トピック                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| オンライン店舗に類別を追加します。 | [オンライン店舗で指定した製品を含む類別を追加します。                                                                  | [設定オンライン店舗] (https://technet.microsoft.com/en-us/library/jj682095.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)                                                                                                                                               |
| カタログを管理します。                     | [店舗で提供する製品を識別する、製品カタログを使用します。                                                              | [目標、: Retailの製品カタログ作成します。] (https://technet.microsoft.com/en-us/library/jj728712.aspx) (Microsoft Dynamics AX 2012のTechNetの内容を)                                                                                                                            |
| 価格を管理します。                       | 価格間で中央のリンクと割引があり、チャンネル、カタログ、所属、ロイヤルティ プログラムの設定および使用して、価格グループ。 | [価格グループ] (https://technet.microsoft.com/en-us/library/hh597169.aspx) (Microsoft Dynamics AX 2012) [設定の詳細]を使用した設定の価格 (https://technet.microsoft.com/en-us/library/hh580571.aspx) (Microsoft Dynamics AX 2012のTechNetの内容) のTechNetの内容 |
| 割引を管理します。                    | 割引の価格調整および4種類の設定および管理します。                                                                                  | [設定の価格調整と割引] (https://technet.microsoft.com/en-us/library/hh597114.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)                                                                                                                           |
| 出荷費用を管理します。             | オンライン店舗に固有の出荷費用を設定および管理します。                                                                     | オンライン[店舗] (https://technet.microsoft.com/en-us/library/jj728714.aspx) (Microsoft Dynamics AX 2012のTechNetの内容) の出荷の設定                                                                                                                           |
| 荷渡方法を管理します。            | その荷渡方法は、オンライン店舗のサービス管理します。                                                                                        | [設定]荷渡方法 (https://technet.microsoft.com/en-us/library/jj728719.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)                                                                                                                                             |

## <a name="set-up-data-exchange-between-dynamics-365-for-operations-and-the-online-store"></a>工程とオンライン店舗365 for Operations間でデータ交換を設定します。
| タスク                                 | 細目                                                                                                                               | トピック                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| チャンネルの統合のプロファイルを設定します。 | プロファイルは、Retailのコンポーネントが会社間の通信を可能にします。 データ交換設定をコンフィギュレーションする前に設定します。 | [設定リアルタイム サービス プロファイル] (https://technet.microsoft.com/en-us/library/hh580631.aspx) (Microsoft Dynamics AX 2012) [設定のTechNetの内容チャンネルのプロファイル] (https://technet.microsoft.com/en-us/library/jj677402.aspx) (Microsoft Dynamics AX 2012のTechNetの内容)  |

 


