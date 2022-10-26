---
title: システムに対して Sensor Data Intelligence を有効にする
description: この記事では、システムに対して Sensor Data Intelligence を有効にする方法について説明します。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 68b9daa6ffdc50d28f746cae060efc1a97ccd57a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689970"
---
# <a name="turn-on-sensor-data-intelligence-for-your-system"></a>システムに対して Sensor Data Intelligence を有効にする

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

## <a name="video-instructions"></a>ビデオの指示

次のビデオでは、センサー データ インテリジェンス機能を有効にし、[必要な Azure リソースを配置する](sdi-deploy-iot-solution-on-azure.md)方法を説明します。 この記事の他のセクションでは、テキスト ベースの形式で同じ手順を示します。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>手順

Sensor Data Intelligence を使用する前に、システムで有効化する必要があります。

1. **システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。 (詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。)
1. **すべて** タブで、**フィルタ** フィールドを 使用して、*Sensor Data Intelligence* という名前の機能 を検索します。
1. システムで *Sensor Data Intelligence* 機能が有効になっている場合は、一覧で選択し、**無効** を選択して無効にします。 この古いバージョンの機能を、次のステップで有効にする新しいプレビュー バージョンと組み合わせて使用することはできません。
1. **フィルター** フィールドを使用して、*(プレビュー) Sensor Data Intelligence* という名前の機能を検索します。
1. リストの機能を選択するには、**今すぐ有効化** を選択して有効化します。
