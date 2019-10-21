---
title: 番号順序スコープの拡張
description: このトピックでは、開発者が番号シーケンスのスコープを拡張する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 04/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 10031
ms.assetid: 4be8b7a1-9632-4368-af41-6811cd100a37
ms.search.region: Global
ms.author: lgou
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b066d323f229d1d328490d07627271614d2aed32
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183330"
---
# <a name="extend-the-scope-of-number-sequences"></a>番号順序スコープの拡張

[!include [banner](../includes/banner.md)]

このトピックでは、数値シーケンスのスコープを拡張する方法を示します。

数字シーケンスの範囲は、数字シーケンスを使用する組織を定義します。 範囲は、**共有**、**会社**、**法人**、または**作業単位**のいずれかにすることができます。 **会社**と**法人**スコープを会計カレンダー期間と組み合わせて、より具体的な番号順序を作成することができます。 新しい番号順序の範囲は、拡張機能を通じて追加できます。  

新しいスコープを作成してクライアントに表示させるには、次の手順を実行します。

1. **NumberSeqParameterType** の列挙型拡張を作成します。 拡張機能に、新しいスコープ タイプの新しい列挙値を追加します。 
2. **NumberSequenceType** の列挙型拡張を作成します。 新しいスコープ タイプの新しい列挙値を追加します。 **NumberSequenceType** 列挙は、**NumberSequenceTableEntity** および **NumberSequencesReferenceEntity** で使用されます。
3. **NumberSequenceScope** テーブル拡張子を作成します。 新しいスコープ タイプの新しいフィールドを追加します。
4. **NumberSeqScope** クラスの拡張クラスを作成します。
   1. **NumberSeqScope::getValidScopeTypes** メソッドのポスト ハンドラーを作成します。 イベント ハンドラー メソッドでは、有効なスコープ タイプのリストに新しいスコープ タイプを追加します。
   1. **onGetFormatSegmentShortName** デリゲートのイベント ハンドラーを作成します。 イベント ハンドラーで、新しいスコープ タイプの短縮名を返します。
   1. **NumberSeqScope::find** メソッドのポスト ハンドラーを作成し、対応する **NumberSeqScope** インスタンスが見つかるように新しいスコープ タイプのロジックを追加します。   
   1. **NumberSeqScope::getId** メソッドのポスト ハンドラーを作成し、新しいスコープ タイプのロジックを追加すると、**NumberSequenceScope** テーブルに対応するレコードが見つかる (存在しない場合は作成される) ようになります。 
5. **NumberSequenceScopeFactory** クラスの拡張クラスを作成します。 新しいスコープ タイプを表す新しい **NumberSeqScope** を初期化するメソッドを追加します。
6. **NumberSequenceDetails** フォームのフォーム拡張を作成します。 **スコープ** タブに新しいスコープ タイプを表示するコントロールを追加します。
7. **NumberSequenceDetails** フォームの拡張クラスを作成します。
   1. 新しいスコープ タイプが**スコープ**ボックスで選択されたときに新しいスコープ タイプを表示するために、**updateScopeControlVisibility** メソッドのポスト ハンドラーを作成します。
   2. **updateScopeControlValues** メソッドのポスト ハンドラーを作成して、**スコープ**タブのコントロールの値を更新します。
   3. 新しいスコープ タイプが選択されたときに **NumberSeqScope** インスタンスを初期化するための **createScope** メソッドのポスト ハンドラーを作成します。
   4. 新しいスコープ タイプの短い名前を返す **getShortNameForParameterType** デリゲートのイベント ハンドラーを作成します。
8. **NumberSequenceTableEntity** および **NumberSequencesReferenceEntity** データ エンティティの拡張クラスを追加します。 新しいスコープ タイプの **NumberSequenceScope** を生成するために、**GenerateNumberSequenceScopeTypes** メソッドと **GenerateNumberSequenceScopeValues** メソッドのポスト ハンドラーを作成します。


