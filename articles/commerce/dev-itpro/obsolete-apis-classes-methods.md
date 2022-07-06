---
title: 廃止または削除された API、クラス、メソッド
description: この記事では、Microsoft Dynamics 365 Commerce で廃止および削除された API、クラス、およびメソッドを一覧表示します。
author: mugunthanm
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 05-24-2022
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 7bb6155cd7c8e2920e8e7bf6258b25085ebeeb23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860275"
---
# <a name="obsolete-and-removed-apis-classes-and-methods"></a>廃止または削除された API、クラス、メソッド

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で廃止および削除された API、クラス、およびメソッドを一覧表示します。

Dynamics 365 Commerce では、いくつかの API、クラス、およびメソッドが、削除済みもしくは廃止としてマークされています。 Dynamics 365 Commerce は時間の経過と共に変化するため、新しいバージョンごとに新しい機能を提供する API、クラス、およびメソッドが追加されます。 既存の API、クラス、およびメソッドも、時間の経過と共に変化します。 たとえば、一部の API は、サポートする機能が新しい機能に置き換えられるため重要性が低くなりますが、他のメソッドは、何らかの点で優れている、または異なる基盤テクノロジーを使用してパフォーマンスと信頼性を向上させる新しいメソッドに取って代わられます。

Dynamics 365 Commerce は、あるバージョンの Commerce を使用して開発された拡張機能を次のバージョンで実行できるように、下位互換性のサポートに務めています。 ただし、下位互換性を使用すると、API、クラス、またはメソッドの削除は困難になります。 代わりに、Dynamics 365 Commerce は、API、クラス、メソッドを廃止または非推奨としてマークし、使用しないようにすることを示します。 (*廃止* および *非推奨* という用語は、.NET タイプとメンバーに適用される場合、同じ意味を持ちます。) このようにして、開発者は API、クラス、またはメソッドがなくなることを認識し、削除の準備をする時間を持つことができます。 

## <a name="obsolete-attribute"></a>廃止された属性

Dynamic 365 Commerce では、API、クラス、またはメソッドは、**廃止** 属性を適用することにより、廃止としてマークされます。 この属性は、API、クラス、メソッドが、今後の Dynamic 365 Commerce のバージョンで削除されることを示します。

## <a name="handling-obsolete-types-and-members"></a>廃止タイプとメンバーの処理

既存のコードをアップグレードして再コンパイルする際に、拡張機能で廃止された API、クラス、またはメソッドを使用すると、コンパイラの警告メッセージが表示される場合があります。 ただし、廃止された API、クラス、またはメソッドは、削除されるまで使用できます。 ただし、警告メッセージを確認して、拡張コードを変更するかどうかを決定する必要があります。 警告メッセージが適切な代替手段を示さなかった場合は、次のいずれかの手順に従う必要があります。

- 可能であれば、API、クラス、またはメソッドが使用されないようにコードを変更してください。
- この領域のドキュメントを確認して、廃止に対応する方法を決定してください。

## <a name="obsolete-and-removed-apis-classes-and-methods-for-hardware-station-hws"></a>廃止または削除されたハードウェア ステーション (HWS) の API、クラス、メソッド

| 廃止または削除された API、クラス、メソッド | 廃止されたバージョン | 変更の理由 | 推奨されるアクション | API、クラス、およびメソッドがソース コードから削除されるバージョン | サンプル コード |
| ------ | ------ |------ |------- |------ |------ |
GenericWarningEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) | 
GenericInformationEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) |
GenericDebugEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) |
ExtendedCriticalEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) |
ExtendedErrorEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) |
ExtendedWarningEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) |
ExtendedInformationalEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) |
ExtendedVerboseEvent | 10.0.14 | 拡張機能は、Application insights を使用してイベントをログに記録する必要があります。 | API、クラス、またはメソッドが使用されなくなるようにコードを変更してから、独自の Application Insights インスタンスを使用して、イベントをログに記録します。 | 10.0.33 | [拡張イベントを Application Insights に記録する](commerce-application-insights.md) |
