---
title: 一方のラインに既に積荷がある
description: このページでは、"一方のラインに既に積荷がある" というエラーを受け取ることのある理由について説明します。 倉庫にリリースできません" というエラーとその問題の解決方法。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476926"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>一方のラインに既に積荷がある

## <a name="symptoms"></a>現象

積荷構築および出荷の作業中に、次のエラー メッセージが表示されることがあります。

> 一方のラインに既に積荷があります。 倉庫にリリースできません。

手動で積荷を作成する場合、または販売注文明細行のエントリが発生する前に積荷を作成するようにプロセスを設定した場合は、後続のリリースが手動で行われること、および積荷からの工順と評価が使用されることを前提としています。

倉庫に対して自動リリースを実行しようとしたが、ウェーブ プロセスで作業を作成できなかった、というシナリオも考えられます。 したがって、この場合も未処理の出荷または積荷が作成されます。 その場合、未処理の出荷または積荷を削除するか、ウェーブを手動で再処理するまで、この未処理の出荷または積荷により、自動的に注文をリリースする試みがブロックされます。

## <a name="resolution"></a>解決策

倉庫へのリリース前に積荷が存在しない場合にのみ、販売注文ページからリリースするか、販売注文のリリース ページから自動リリースを行うことができます。 ウェーブが処理されると、自動的に積荷が作成されます。
