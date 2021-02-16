---
title: 静的ファイルのアップロードと提供
description: このトピックでは、静的ファイルを Microsoft Dynamics 365 Commerce サイト ビルダーにアップロードする方法と、そのファイルを要求するために使用できるカスタム URL およびファイル名の作成方法について説明します。
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594979"
---
# <a name="upload-and-serve-static-files"></a>静的ファイルのアップロードと提供

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、静的ファイルを Microsoft Dynamics 365 Commerce サイト ビルダーにアップロードする方法と、そのファイルを要求するために使用できるカスタム URL およびファイル名の作成方法について説明します。

サードパーティの一部のコネクタでは、電子商取引サイトからファイルをホストし、提供する必要があります。 これらのコネクタは、特定のコールバック URL パスとファイル名への要求によってファイルが返されることを予期しています。 したがって、このトピックでは、Dynamics 365 Commerce 電子商取引サイト上にユーザー定義可能な URL とファイル名を持つ静的ファイルをアップロードして提供する方法について説明します。

## <a name="create-a-site-url-that-returns-a-static-file"></a>静的ファイルを返すサイト URL の作成

Commerce サイト ビルダーで静的ファイルを返すサイトの URL を作成するには、次の手順を実行します。

1. サイトのメディア ライブラリに移動し、定義する URL に要求によって提供する必要があるファイルをアップロードします。 ファイルが既にアップロードされている場合は、この手順を省略できます。
1. サイトの **URL** に移動します。
1. **新規 \> 新しい URL** を選択します。
1. **新しい URL** ダイアログ ボックスで、**メディア ライブラリ アセット** を選択します。
1. **URL パス** フィールドに URL パスを入力します。 パスにファイル名を含めます。
1. **次へ** を選択します。 メディア ライブラリが開き、アップロードされた **ドキュメント** タイプのすべてのメディア アセットが表示されます。
1. 手順 5 で定義した URL への要求に対して提供するファイルを選択します。
1. **保存** を選択します。

この時点で、作成した URL はドラフト状態になっています。 URL をポイントしたファイルは、URL を発行するまで返されません。 URL を発行する前に、適切なデータを返すかどうかを検証できます。

## <a name="validate-and-publish-a-url"></a>URL の検証と発行

発行前に URL を検証するには、次の手順を実行します。

1. サイトの **URL** に移動し、プレビューする URL を選択します。
2. 右側のプロパティ ウィンドウで、**編集** ボタンの下にある適切な URL リンクを選択します。 新しいブラウザー ウィンドウが開き、404 エラーが表示されます。
3. URL に **?preview=inprogress** クエリ文字列を追加し (例: `https://yoursite.com/callback.html?preview=inprogress`)、ページを再読み込みします。 メディア ライブラリにアップロードしたファイルが応答に含まれている必要があります。

URL を検証したら、それを公開できます。

1. サイトの **URL** に移動し、URL を選択します。
2. コマンド バーで **発行** を選択します。

## <a name="update-the-file-that-a-url-points-to"></a>URL がポイントするファイルの更新

URL が発行されたら、それを更新して、別のファイルを指すようにすることができます。 または、次のセクションで説明するように、異なるタイプのリソースをポイントするように URL を更新することもできます。 たとえば、URL を内部ページまたはリダイレクトにポイントすることができます。

URL で指定されているファイルを更新するには、次の手順を実行します。

1. サイトの **URL** に移動し、更新する URL を選択します。
1. 右側のプロパティ ウィンドウで、**編集** を選択します。
1. **URL の割り当て** で、**ステップ 2** ボックスをオンにし、メディア ライブラリから新しいドキュメントを選択します。
1. **適用** を選択します。

## <a name="update-the-asset-type-that-a-url-points-to"></a>URL がポイントするアセット タイプの更新

URL を更新して、内部ページまたはリダイレクトなどの別のタイプのアセット (リソース) をポイントするようにすることもできます。

URL で指定されているアセット タイプを更新するには、次の手順を実行します。

1. サイトの **URL** に移動し、更新する URL を選択します。
1. 右側のプロパティ ウィンドウで、**編集** を選択します。
1. **URL の割り当て** の **ステップ 1** で、別のアセット タイプを選択します。
1. **ステップ 2** ボックスをオンにし、新しいアセットを選択します。
1. **適用** を選択します。

## <a name="change-the-url-path"></a>URL パスの変更

URL が作成された後は、パスを変更することはできません。 ファイルまたはその他の種類のリソースに対応する URL パスを変更する必要がある場合は、新しい URL を作成し、既存のファイルまたはその他のリソースにマップしてから、古い URL を発行解除して削除する必要があります。

URL パスを変更するには、次の手順に従います。

1. 新しい URL を作成して既存のファイルまたは別のリソースにマップするには、このトピックの前の[静的ファイルを返すサイト URL を作成する](#create-a-site-url-that-returns-a-static-file)セクションの手順に従ってください。
1. 新しい URL を選択し、コマンド バーの **発行** を選択します。 新しい URL が発行されます。
1. 古い URL の発行を解除するには、URL を選択し、コマンド バーの **発行取り消し** を選択します。 古い URL を必要に応じて削除できるようになりました。

## <a name="additional-resources"></a>追加リソース

[デジタル資産管理の概要](dam-overview.md)

[画像のアップロード](dam-upload-images.md)

[ビデオのアップロード](dam-upload-video.md)

[画像とビデオ以外のファイルのアップロード](dam-upload-files.md)

[画像のトリミング](dam-crop-images.md)

[画像の中心のカスタマイズ](dam-custom-focal-point.md)
