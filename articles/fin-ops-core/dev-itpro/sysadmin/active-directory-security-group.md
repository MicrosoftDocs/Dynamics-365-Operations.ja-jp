---
title: Active Directory セキュリティ グループ
description: この記事では、Active Directory セキュリティ グループ機能に関する情報について説明します。
author: peakerbl
ms.date: 11/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2022-11-10
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: 5bab02b0c905c90500834966dc2edae190584c6a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780309"
---
# <a name="active-directory-security-groups"></a>Active Directory セキュリティ グループ

[!include [banner](../includes/banner.md)]

**Active Directory セキュリティ グループ** は、Microsoft Active Directory セキュリティ グループのメンバーシップに基づいてロールおよび組織をユーザーに割り当てできる従来の機能です。 (Active Directory セキュリティ グループの詳細については、[Active Directory セキュリティ グループ](/windows-server/identity/ad-ds/manage/understand-security-groups) を参照してください。) また、この機能を使用すると、財務および運用環境に初めてサインインするときに、ユーザーの just-in-time (JIT) プロビジョニングも可能になります。

グループ ベースのロール割り当ては、ユーザーに対する手動および自動のルール ベースの割り当てを使用して適用されます。 割り当てられたロールの組み合わせによって、実際のデータ アクセスが決まります。

## <a name="known-limitations-when-the-active-directory-security-groups-feature-is-used"></a>Active Directory セキュリティ グループ機能を使用する際の既知の制限

**Active Directory セキュリティ グループ** 機能を有効にする前に、次の既知の制限を認識しておくことが重要です。 いくつかの制限は内部コントロールと監査に影響します。

- 関税レポートの分掌では、これらのロールの割り当ては考慮されません。
- これらのロール割り当てに対してデータベース ログを作成できません。
- セキュリティおよびライセンスのレポートには、これらのロールの割り当ては含まれません。
- ロールの割り当て、**ロールへのユーザーの割り当て** ページ、**選択したユーザーのロール** FactBox を表示するページには、これらのロールの割り当ては含まれません。
- 外部ユーザーはサポートされていません。 JIT プロビジョニングは使用できず、グループ メンバーシップに基づいてロールを割り当てることはできません。
- 割り当てられたロールに依存するワークフローでは、これらのロールの割り当ては考慮されません。
- システム管理でグループを無効にしても、JIT プロビジョニングやロールの割り当ては停止されません。
- JIT プロビジョニングによって作成されたユーザの **ユーザ ID** 値は、先頭にドル記号 ($) と数字が付きます。

Microsoft は、グループ エクスペリエンスが Dataverse のより包括的な機能に統合されるまで、このような既知の制限に対処することは想定していません。 詳細については [グループ チームの管理](/power-platform/admin/manage-group-teams) を参照してください。

## <a name="enable-the-active-directory-security-groups-feature"></a>Active Directory セキュリティ グループ機能の有効化

機能を有効にするには、**システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順に移動します。 **Active Directory セキュリティ グループ** コンフィギュレーション キーは、**管理** フォルダーにあります。

コンフィギュレーション キーは、メンテナンス モードでのみ編集できます。 詳細については、[メンテナンス モード](../sysadmin/maintenance-mode.md) を参照してください。

## <a name="import-and-configure-active-directory-security-groups"></a>Active Directory セキュリティ グループのインポートと構成

機能を有効にすると、**システム管理 \> ユーザー \> グループ** で新しい **グループ** ページを使用できます。 Azure Directory セキュリティ グループのインポートを開始するには、**グループのインポート** を選択し、インポートするグループを選択します。

インポートが完了したら、**グループ** ページでロールと組織の割り当てを管理できます。 このプロセスは、**ユーザー** ページで使用されるプロセスに似ています。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
