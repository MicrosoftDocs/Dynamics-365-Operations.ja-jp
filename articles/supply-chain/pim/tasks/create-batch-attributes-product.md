---
title: 製品のバッチ属性の作成
description: この手順では、バッチ属性の作成方法、既定値の範囲の割り当て方法、グループに属性を含める方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1583bb581845aa60591436ffb8851bd52c359a5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208297"
---
# <a name="create-batch-attributes-for-a-product"></a>製品のバッチ属性の作成

[!include [banner](../../includes/banner.md)]

この手順では、バッチ属性の作成方法、既定値の範囲の割り当て方法、グループに属性を含める方法を示します。 この手順の作成に使用するデモ データの会社は USP2 です。

1. [在庫管理] > [設定] > [バッチ] > [バッチ属性] の順に移動します。
2. [新規] をクリックします。
3. [属性] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [属性タイプ] フィールドで、「属性」を選択します。
    * この手順では、小数値を有効にするために [小数] タイプを使用します。 他の属性タイプを選択することもできます。 列挙型を選択する場合、ターゲット フィールドに値を入力する前に、列挙型リストで値を入力する必要があります。  
6. [最小] フィールドに数値を入力します。
7. [最大] フィールドに数値を入力します。
8. [増分] フィールドに数値を入力します。
9. [ターゲット] フィールドに値を入力します。
10. [保存] をクリックします。
11. ページを閉じます。
12. [在庫管理] > [設定] > [バッチ] > [バッチ属性グループ] の順に移動します。
13. [新規] をクリックします。
14. [属性グループ] フィールドに値を入力します。
15. [説明] フィールドに値を入力します。
16. [保存] をクリックします。
17. [グループ属性] をクリックします。
18. [新規] をクリックします。
19. [属性] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
20. 一覧で、目的のレコードを見つけ、選択します。
21. 一覧で、選択された行のリンクをクリックします。
    * 属性は、いずれかのグループに含めることができます。  
22. [保存] をクリックします。
23. ページを閉じます。

