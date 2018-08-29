---
title: "ラベル拡張ファイルを使用してラベルを変更します"
description: "このトピックでは、ラベル拡張ファイルを作成してラベルの文字列値を変更する方法、同じラベル ファイルに新しいラベルを追加する方法、または新しい言語を追加する方法について説明します。"
author: smithanataraj
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5e6856476e532e7e50f656f0e64d013d0e5aa03c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="change-labels-by-using-label-extension-files"></a>ラベル拡張ファイルを使用してラベルを変更します

[!include [banner](../includes/banner.md)]

ラベルの文字列値を変更、同じラベル ファイルに新しいラベルを追加、または新しい言語を追加する、ラベル拡張ファイルを作成することができます。 ラベル拡張ファイルの名前は、ラベル ファイルの名前に **\_extension** の接尾語を加えたものでなければなりません。 

次の例は、AccountsPayable ラベルファイルを拡張して、ウェールズ語を新しい言語として追加する方法を示しています。
 
1. 新しいラベル拡張を追加する必要があるモデルに属するプロジェクトを作成します。 この例では、プロジェクトは **ApplicationSuite** と名前が付けられます。
1. プロジェクトに新しいラベル ファイルを追加し、**AccountsPayable_Extension** という名前をつけます。 ラベル ファイルを追加した後、**ラベル ファイル** ウィザードが起動します。

    ![ラベル ファイル ウィザード: ラベル ファイル ID ページの指定](media/ExtendLabel01.png)

2. ウィザードの次のページで、拡張機能の一部となる言語を選択します。 この例では、**英語 (米国)** (**EN-US**) が既に基本言語となっており、**ウェールズ語** (**cy**) を追加しました。

    ![ラベル ファイル ウィザード: 言語ページの選択](media/ExtendLabel02.png)

3. ウィザードの操作を完了します。 次の図に示すように、2 つのラベル拡張ファイルが作成されます。

    ![ラベル拡張ファイル](media/ExtendLabel03.png)

4. この例の拡張ファイルでは、新しいラベルを作成したり、アプリケーション スイート モデルの **AccountsPayable** で定義されているラベルの値を変更したりできます。 新しいラベルを定義するか、既に存在するラベルを再定義するには、標準のラベル エディタを使用します。
5. 任意の時点で、ラベル ファイルにその他の言語を追加できます。 プロジェクトで名前が **\_extension** で終わるラベル ファイルを右クリックしてから、**新しい言語の追加**を選択します。 その後、翻訳ファイルを追加するウィザードに従います。

