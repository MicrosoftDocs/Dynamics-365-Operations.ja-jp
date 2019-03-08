---
title: 作業クラスの作成
description: この手順では、作業クラスを設定する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5def9be0966d65728ffb0897229c0d749e7e13a0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "356027"
---
# <a name="create-a-work-class"></a>作業クラスの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、作業クラスを設定する方法を示します。 作業クラスは、倉庫作業者がモバイル デバイスで処理できるワーク オーダー明細行のタイプを指示または制限するために使用されます。 作業者が処理できる明細行は、倉庫作業者がアクセス権を持つモバイル デバイスの作業クラスと、作業明細行に指定された作業クラスにより決定されます。 また、作業クラスは、ワーク オーダー明細行に対して設定されている場所を検証するために使用できます。 この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。 この手順は、倉庫マネージャーを対象としています。

1. [倉庫管理] > [設定] > [作業] > [作業クラス] に移動します。
2. [新規] をクリックします。
3. [作業クラス ID] フィールドで、値を入力します。
4. [説明] フィールドに値を入力します。
5. [ワーク オーダー タイプ] フィールドで、オプションを選択します。
6. [新規] をクリックします。
7. [場所タイプ] フィールドに値を入力します。
    * 場所のタイプを選択すると、ピッキング後に品目を配置できる場所の制限が設定されます。 この設定は、場所のディレクティブが場所を解決しようとする場合、または倉庫作業者がモバイル デバイスのメニュー項目に手動で場所を提供する場合に使用されます。  
8. ページを閉じます。

