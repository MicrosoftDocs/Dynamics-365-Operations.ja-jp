---
title: クラスとメソッドの属性を使用した SysTest フィルタリング
description: このトピックでは、テストのフィルター処理の目的で SysTest クラスおよびメソッドで使用できる属性について説明します。
author: jorisdg
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-11-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ba1e5b481efa869e461b9c828fd12403facc092
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781945"
---
# <a name="systest-filtering-using-class-and-method-attributes"></a>クラスおよびメソッドの属性を使用した SysTest フィルター処理

[!include [banner](../includes/banner.md)]

プラットフォーム更新プログラム 12 以降、SysTest フレームワークには、X++ で SysTest クラスおよびメソッドの属性の強化が含まれています。 これらの機能強化により、これらの属性が、Visual Studio テスト ウィンドウおよび自動ビルドプロセスで使用されるツールである Visual Studio テスト コンソールでどのように機能するかも変わります。 SysTest フレームワークは、MSTest フレームワーク アダプターと同等になるように、アダプター内の主要なテスト属性をサポートするようになりました。 これには **カテゴリ**、**所有者**、**優先順位**、および **テスト プロパティ** などの属性が含まれます。

## <a name="testcategory"></a>TestCategory

**カテゴリ** 属性である **SysTestCategory** は、**SysTestCategory** 属性を使用した以前のプラットフォーム更新プログラムですでに利用可能でした。 プラットフォーム更新プログラム 12 以降、クラス レベルと個々のメソッド レベルの両方で複数のカテゴリを指定できます。 さらに、**TestCategory** では、Visual Studio テスト コンソールでのフィルター処理が有効になっています。 つまり、特定のカテゴリのテスト フィルターを使用して、ビルド パイプラインを作成できます。 ビルド パイプラインで、**TestFilter** 変数を使用できます。 たとえば、カテゴリ **Nightly** でのみテストを実行するには、変数を **TestCategory=Nightly** に設定します。

## <a name="priority"></a>優先順位

整数値を必要とする **Priority** 属性の **SysTestPriority** が利用可能になりました。 優先順位は 1 回のみ指定できますが、クラスとメソッドの両方のレベルでサポートされ、メソッド レベルはクラス レベルよりも優先されます。 優先順位は、テスト フィルターとしても公開されます。 したがって、ビルド パイプラインで、**TestFilter** 変数を使用できます。 たとえば、優先順位 **1** でのみテストを実行するには、変数を **Priority=1** に設定します。

## <a name="owner"></a>所有者

**所有者** 属性である **SysTestOwner** も追加されました。 この属性は技術的には既に **Test Toolbox** ウィンドウでのフィルター処理に対してサポートされていましたが、属性自体は X ++ にはありませんでした。 **Priority** と同様に、所有者は 1 回のみ指定でき、クラスとメソッドの両方のレベルでサポートされ、メソッド レベルが優先されます。 **所有者** は、コンソール用のテストフィルターとしては使用できません。これは、Visual Studio テスト コンソール用の MSTest アダプターに対応しています。 ただし、**所有者** は Visual Studio の **Test Toolbox** ウィンドウに表示されます。

## <a name="test-property"></a>テスト プロパティ

**テスト プロパティ** 属性の **SysTestProperty** は、プラットフォームの以前のリリースに存在していましたが、完全には機能しませんでした。 ただし、**SysTestProperty** 属性は **Test Essentials** パッケージに存在する他の属性とは対照的に、**アプリケーション基準** パッケージに存在します。 プラットフォームの下位互換性への確約のため、現在この属性を予定の場所に移動することはできません。そのため、使用するには **アプリケーション基準** パッケージへの参照が必要になります。 **SysTestProperty** はプロパティと値 (2 つの文字列) を指定し、Visual Studio の **Test Toolbox** ウィンドウで使用できるようになりました。 **テスト プロパティ** は複数回指定でき、クラスとメソッドの両方のレベルで存在できます。 **テスト プロパティ** は、MSTest アダプタに従って、Visual Studio テスト コンソールのフィルター処理のテストには使用できません。

Visual Studio テスト コンソールで使用できる高度なフィルター処理構文および MSTest フレームワークのフィルター処理例の確認については、[選択可能な単位テストの実行](/dotnet/core/testing/selective-unit-tests) を参照してください。 

> [!NOTE]
> フィルター処理のテストの目的で、SysTest フレームワークを使用して **FullyQualifiedName** と **名前** でフィルター処理することができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]