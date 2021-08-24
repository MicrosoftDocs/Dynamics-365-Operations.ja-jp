---
title: エンジニアリング製品のバリアントの生成
description: このトピックでは、エンジニアリング製品のバリアントを生成する方法について説明する
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 57eda6a833df6ff8e91c006bbc5096554eff6c503a8b7ba2bd0b13e2f8e98f56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766154"
---
# <a name="generate-variants-for-engineering-products"></a>エンジニアリング製品のバリアントの生成

[!include [banner](../includes/banner.md)]

このトピックでは、エンジニアリング製品のバリアントを生成する方法について説明します。

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>エンジニアリング製品の 1 つ以上の新しいバリアントの生成

既存の製品からの情報をコピーせずに、製品の 1 つ以上の新しいバリアントを作成できます。 これは、複数の製品バリアントを同時に作成する必要がある場合に便利です。

次の手順では、カラー分析コードを含む複数のバリアントの作成方法の例を示します。

1. **リリース済製品ページ** を開きます (たとえば、**エンジニアリング変更管理 \> 共通 \> リリース済製品** に移動します)。
1. アクション ペインで、**製品** タブを開き、**新規** グループから、**エンジニアリング製品** を選択します。
1. **新しい製品** ダイアログが開きます。 適切な **エンジニアリング カテゴリ** を選択します。
1. 選択したエンジニアリング カテゴリにバリアント分析コードが含まれる場合は、ここで値を設定できます。 たとえば、カテゴリに **カラー** 分析コードが含まれる場合は、*青* に設定できます。
1. 必要に応じてその他の設定を行います。 **OK** を選択して製品を作成します。
1. 製品と青 V-1 バリアントが作成され、新しい製品が開きます。
1. 必要に応じて、部品表 (BOM) およびルートをバリアントに追加します。
1. アクション ペインで、**製品** タブを開き、**製品マスター** グループにある **製品分析コード** を選択します。
1. **製品分析コード** ページが開きます。 このページには、使用可能な各分析コードのタブが含まれます。 各タブで、各関連する分析コードでサポートする値ごとに行を追加します。 (この例では、*白*、*黄*、および *緑* の **カラー** タブで行を追加できます)。
1. ページを閉じて、**リリース済製品バリアント** を選択します。 最初に作成したバリアント (白 V-1) が表示されます。
1. **バリアント提案** を選択します。
1. 作成した色の値 (たとえば、白 V-1、黄 V-1、および緑 V-1) を持つバリアントがシステムによって提案されます。
1. 提案されるバリアントを選択してから **OK** を選択し、そのバリアントをエンジニアリング会社にリリースします。 次の条件が適用されることに注意してください: 
    - 作成されたバリアントに BOM またはルートがありません。
    - これらのバリアントの属性は、既定ではエンジニアリング カテゴリから取得され、前のバリアントからはコピーされません。

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>別の製品バリアントのコピーとしてバリアントを生成する

別の製品バリアントに基づいて製品のバリアントを作成できます。 ソース製品バリアントの部品表 (BOM) およびルートが新しいバリアントにコピーされます。 これは、開始 BOM に基づいて BOM を作成し、前のバリアントからの変更を追跡すると便利な個別の製造製品に役立つ場合があります。 追跡を管理するために、システムはどのバリアントがコピーされたかを記録して、新しいコピーを作成します。

次の手順は、既存のバリアントのコピーを作成することにより、カラー分析コードを含む新しいバリアントを作成する方法の例を提供する

1. **リリース済製品ページ** を開きます (たとえば、**エンジニアリング変更管理 \> 共通 \> リリース済製品** に移動します)。
1. アクション ペインで、**製品** タブを開き、**新規** グループから、**エンジニアリング製品** を選択します。
1. **新しい製品** ダイアログが開きます。 適切な **エンジニアリング カテゴリ** を選択します。
1. 選択したエンジニアリング カテゴリにバリアント分析コードが含まれる場合は、ここで値を設定できます。 たとえば、カテゴリに **カラー** 分析コードが含まれる場合は、*青* に設定できます。)
1. 必要に応じてその他の設定を行います。 **OK** を選択して製品を作成します。
1. 製品と青 V-1 バリアントが作成され、新しい製品が開きます。
1. 必要に応じて、BOM およびルートをバリアントに追加します。
1. 必要に応じて、属性を製品バリアントに追加します。
1. 青 V-1 製品バリアントを、エンジニアリング変更オーダーに追加します。
1. **影響** を *新しいバリアント* に設定します。
1. 新しい色の値 (たとえば、*白*) を選択します。 次の条件が適用されることに注意してください: 
    - 新しいバリアントには、前のバリアントからコピーされた BOM およびルートがあります。
    - 新しいバリアントには、以前のバリアントからコピーされた属性があります。
1. 変更オーダーの承認。
1. 変更オーダーのプロセス。 オーダーが処理された後、新しい V-1 バリアントが作成され、エンジニアリング会社にリリースされます。