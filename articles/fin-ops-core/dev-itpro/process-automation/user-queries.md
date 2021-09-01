---
title: 構成可能なユーザーのクエリ
description: このトピックでは、構成可能なクエリを作成し、プロセス自動化フレームワークで使用する方法について説明します。
author: RyanCCarlson2
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a247ce22fbaed2657d52923fa8982b82755b1e033cbba14b7993237afb7ffbfd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738498"
---
# <a name="user-configurable-queries"></a>構成可能なユーザーのクエリ

[!include [banner](../includes/banner.md)]

このトピックでは、構成可能なクエリを作成し、プロセス自動化フレームワークで使用する方法について説明します。 プロセスが **SysQueryForm** フォームによるユーザーの構成可能なクエリをサポートしていない場合は 、このタスクを省略できます。

プロセス自動化フレームワークでは、**SysQueryForm** フォームを介したカスタム クエリのサポートが制限されています。 カスタム クエリを使用すると、ユーザーはカスタムの基準を追加して、プロセスの実行方法を制限することができます。 フレームワークには、ユーザーが指定したカスタムの基準を抽出するためのロジックと、それらの基準を格納するためのテーブルがあります。 カスタム クエリ基準は、指定された一連の発生ごとに格納され、個別に変更できます。 フレームワークには、各発生のプロセスの実行に使用されるクエリにカスタム基準を適用するための API も用意されています。

> [!NOTE]
> ユーザーがクエリ基準を適用するときには、すべてのクエリ オブジェクトは保存されません。 代わりに、クエリ基準は個別に保存され、クエリの拡張機能のサポートが強化されます。 したがって、この方法を使用する場合、既存のクエリ基準の既存のクエリに対する拡張機能によって破壊的変更が発生することはありません。 この場合、新しい拡張機能では、保存されたシリーズまたは発生にクエリ基準を変更または再作成する必要はありません。 ただし、クエリ基準の変更または再作成は可能です。

## <a name="processscheduleiqueryable-interface"></a>ProcessScheduleIQueryable インターフェイス

**ProcessScheduleIQueryable** インターフェイスは、元のクエリ (ユーザーによって変更される前のクエリ) とユーザーが変更したクエリを取得します。 これらのクエリは、プロセスの実行時に基準を適用するため、またはユーザーが変更を行うときに基準を抽出するために使用されます。 これらの基準は、プロセス自動化フレームワークによって格納されます。

このインターフェイスは、プロセス自動化の指定された実装の基準フォームでアクセスされます。 このインターフェイスへのアクセス例については、**VendPaymProposalAutomationCriteria** フォームを参照してください 。 このフォームには、**SysQueryForm** フォームのサンプル実装も含まれてい ます。

| メソッド | 説明 |
|---|---|
| `public Query getOriginalQuery()` | このメソッドは、変更されていない元のクエリを取得して、比較基準として使用します。 |
| `public Query getQueryForApplicationOrExtractionOfQueryCriteria()` | このメソッドは、変更済みかまたは変更される予定のクエリを取得して、クエリ基準を適用または抽出するために使用します。 |

> [!NOTE]
> **ProcessScheduleIQueryable** の実装に使用されるクエリは、自動化する基になるプロセスの実行時に使用されるクエリと同じ構造を持つ必要があります。 本質的に付加されない構造的な誤差があると、保存されたクエリ基準がランタイムに適用されると、ランタイム エラーが発生します。 クエリの構造が変わらないようにするには、設計されたクエリを使用するか、クエリを構築する共有ロジックを使用する必要があります。

## <a name="processschedulequerycriteriaapplicator-class"></a>ProcessScheduleQueryCriteriaApplicator クラス

**ProcessScheduleQueryCriteriaApplicator** クラスは、特定の発生に対して保存されているクエリ基準を、プロセスの実行時に使用されるクエリのランタイム インスタンスに適用するために使用されます。 この API は、実行中にクエリが保存された基準を受け入れる準備ができた時点で、取り込みプロセスによって呼び出される必要があります。 クエリを構築する設計されたクエリまたは共有ロジックが使用されている場合、この呼び出しは通常、クエリが正しく初期化された後に発生します。 この API がどのように使用されるかを示す例については、**CustVendCreatePaymJournal.constructFromAutomationExecutionContract** メソッドを参照してください 。

| メソッド | 説明 |
|---|---|
| `public static void applyCriteriaForOccurrenceExecution(Query _queryToApplyCriteria, RefRecId _scheduleOccurrenceRecId)` | |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]