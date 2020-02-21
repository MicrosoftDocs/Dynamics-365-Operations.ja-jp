---
title: ページ上またはグリッド内の画像
description: このトピックでは、画像をページまたはグリッドに表示する手順について説明します。 このトピックでは、イメージの使用方法のいくつかについての背景と、使用される API についても説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 55871
ms.assetid: 58e6476b-c29f-46c4-8866-78ca4ab3c0bc
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff856486c965179edcf121abb07c7584451759ee
ms.sourcegitcommit: 9f90b194c0fc751d866d3d24d57ecf1b3c5053a1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3033032"
---
# <a name="images-on-a-page-or-in-a-grid"></a><span data-ttu-id="7235b-104">ページ上またはグリッド内の画像</span><span class="sxs-lookup"><span data-stu-id="7235b-104">Images on a page or in a grid</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7235b-105">このトピックでは、画像をページまたはグリッドに表示する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="7235b-105">This topic describes the steps for displaying images on a page or in a grid.</span></span> <span data-ttu-id="7235b-106">このトピックでは、イメージの使用方法のいくつかについての背景と、使用される API についても説明します。</span><span class="sxs-lookup"><span data-stu-id="7235b-106">The topic also provides background about some of the ways that images can be used, and the APIs that are used.</span></span>  

> [!NOTE]
> <span data-ttu-id="7235b-107">アクセシビリティのために、画像を使用して状態を示したり、データを表示するときには、その画像が表す値または状態を説明するツールヒント、拡張プレビュー、ラベル、またはその他のテキスト形式表記が添付されていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7235b-107">For accessibility, when you use an image to indicate status or show data, the image must be accompanied by a tooltip, enhanced preview, label, or other textual representation that describes the value or status that the image represents.</span></span> 

<span data-ttu-id="7235b-108">Finance and Operation アプリでは、イメージに埋め込みリソースを使用しません。</span><span class="sxs-lookup"><span data-stu-id="7235b-108">Finance and Operation apps do not use embedded resources for images.</span></span> <span data-ttu-id="7235b-109">代わりに、ライトウェイト記号を使用します。</span><span class="sxs-lookup"><span data-stu-id="7235b-109">Instead, it uses lightweight symbols.</span></span> <span data-ttu-id="7235b-110">新しいイメージ コントロールをサポートするために、コーディング パターンがわずかに変更されました。</span><span class="sxs-lookup"><span data-stu-id="7235b-110">The coding pattern has changed slightly to support the new image control.</span></span> 

<span data-ttu-id="7235b-111">ImageList 使用により、ランタイムは古い **ImageID** 値を受け入れて記号にマップし、既存のコードは引き続き動作できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7235b-111">For ImageList uses, the runtime accepts the old **ImageID** value and maps it to a symbol, so that existing code continues to work.</span></span>

> [!NOTE]
> <span data-ttu-id="7235b-112">場合によっては、ランタイム マッピング後もイメージが存在せず、この動作は意図的です。</span><span class="sxs-lookup"><span data-stu-id="7235b-112">In some cases, there is no image even after runtime mapping, and this behavior is intentional.</span></span> 

<span data-ttu-id="7235b-113">AX 2012 は、ステータスを示すためにグリッド列で画像を表示します。</span><span class="sxs-lookup"><span data-stu-id="7235b-113">AX 2012 displays images in a grid column to indicate status.</span></span> <span data-ttu-id="7235b-114">これらの画像は、利用できなくなった埋め込みリソースから取得されることがありました。</span><span class="sxs-lookup"><span data-stu-id="7235b-114">These images were sometimes retrieved from embedded resources that are no longer available.</span></span> 

<span data-ttu-id="7235b-115">AX 2012は、画像の次の記憶域オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="7235b-115">AX 2012 offers the following storage options for images:</span></span>

-   <span data-ttu-id="7235b-116">画像がカーネル自体の一部として提供される埋め込みリソース</span><span class="sxs-lookup"><span data-stu-id="7235b-116">An embedded resource where images are offered as part of the kernel itself</span></span>
-   <span data-ttu-id="7235b-117">Application Object Server (AOS) リソースは開発者または独立系ソフトウェア ベンダー (ISV) が独自のイメージ リソースを追加できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-117">An Application Object Server (AOS) resource where developers or independent software vendors (ISVs) can add their own image resources</span></span>
-   <span data-ttu-id="7235b-118">実行時に開発者または ISV が画像を読み込むファイルの場所</span><span class="sxs-lookup"><span data-stu-id="7235b-118">A file location where developers or ISVs can load images at run time</span></span>
-   <span data-ttu-id="7235b-119">ビットマップとして保存されているデータベース フィールド</span><span class="sxs-lookup"><span data-stu-id="7235b-119">A database field that is stored as a bitmap</span></span>

<span data-ttu-id="7235b-120">次の記憶域オプションは、イメージに使用できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-120">The following storage options are available for images:</span></span>

-   <span data-ttu-id="7235b-121">AOS リソースは開発者や ISV が独自のイメージ リソースを追加できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-121">An AOS resource where developers or ISVs can add their own image resources</span></span>
-   <span data-ttu-id="7235b-122">実行時に開発者または ISVs が画像を読み込む URL の場所</span><span class="sxs-lookup"><span data-stu-id="7235b-122">A URL location where developers or ISVs can load images at run time</span></span>
-   <span data-ttu-id="7235b-123">コンテナーとして保存されているデータベース フィールドです。</span><span class="sxs-lookup"><span data-stu-id="7235b-123">A database field that is stored as a container.</span></span>
-   <span data-ttu-id="7235b-124">画像がフォントの名前でレンダリングされる記号フォント</span><span class="sxs-lookup"><span data-stu-id="7235b-124">A symbol font, where images are rendered by name from the font</span></span>

<span data-ttu-id="7235b-125">AOS リソースとして保存されるイメージは、ユーザー データに分類されていないイメージを使用でき、お使いのアプリケーションと共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-125">Images that are stored as AOS resources allow for the use of an image that isn't categorized as user data, and can be used with your application.</span></span> 

> [!NOTE]
> <span data-ttu-id="7235b-126">UX が使用を承認したレガシ埋め込みリソース イメージがある場合、それらの埋め込みイメージを手動で AOS リソースに転送して使用できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-126">If there are legacy embedded resource images that UX has approved for use, those embedded images can be manually transferred to an AOS resource and used.</span></span> 

<span data-ttu-id="7235b-127">一般的な Web アプリケーションは、Internet Information Services (IIS) サーバー上の画像のコレクションを管理し、画像の URL を提供します。</span><span class="sxs-lookup"><span data-stu-id="7235b-127">A typical web application maintains a collection of images on an Internet Information Services (IIS) server and just provides a URL to the image.</span></span> <span data-ttu-id="7235b-128">この方法はサポートされていますが、非常に多く使用されるとは考えていません。</span><span class="sxs-lookup"><span data-stu-id="7235b-128">Although this approach is supported, we don't expect that it will be used very much.</span></span> <span data-ttu-id="7235b-129">代わりに、記号フォントをイメージ ソースとして使用することを期待します。</span><span class="sxs-lookup"><span data-stu-id="7235b-129">Instead, we expect that the symbol font will be used as an image source.</span></span> 

<span data-ttu-id="7235b-130">もちろん、アプリケーション ロジックは、許可された厳密な従業員の写真、製品画像など、データベースに画像を保管し、この方法は、ファースト クラスの経験です。</span><span class="sxs-lookup"><span data-stu-id="7235b-130">Of course, application logic will store an image in a database to allow for strong employee photos, product images, and so on, and this approach is a first-class experience.</span></span> 

<span data-ttu-id="7235b-131">記号フォントは、最もパフォーマンスが高く、スケーラブルな画像形式です。</span><span class="sxs-lookup"><span data-stu-id="7235b-131">A symbol font is the most performant and scalable image format.</span></span> <span data-ttu-id="7235b-132">ほとんどのアプリケーションのユース ケース (グリッドの行ごとのステータスやボタンの画像など) に記号フォントの文字の使用を考えています。</span><span class="sxs-lookup"><span data-stu-id="7235b-132">We expect that characters from the symbol font will be used for most application use cases (grid row by row status, button images, and so on).</span></span> 

<span data-ttu-id="7235b-133">記号フォントで利用できる記号の一覧については、[記号フォント](symbol-font.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7235b-133">For the list of symbols that are available in the symbol font, see [Symbol font](symbol-font.md).</span></span>

## <a name="image-type-symbol"></a><span data-ttu-id="7235b-134">イメージの種類: シンボル</span><span class="sxs-lookup"><span data-stu-id="7235b-134">Image type: Symbol</span></span>

| <span data-ttu-id="7235b-135">プロ</span><span class="sxs-lookup"><span data-stu-id="7235b-135">Pros</span></span> | <span data-ttu-id="7235b-136">短所</span><span class="sxs-lookup"><span data-stu-id="7235b-136">Cons</span></span> |
|---|---|
| <ul><li><span data-ttu-id="7235b-137">通常、記号フォントは、クライアントに送られる最小のペイロードです。</span><span class="sxs-lookup"><span data-stu-id="7235b-137">Usually, the symbol font is the smallest payload to send to the client.</span></span></li><li><span data-ttu-id="7235b-138">カスケード スタイル シート (CSS) を使用することにより、画像を簡単にカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="7235b-138">You can easily customize the images by using Cascading Style Sheets (CSS).</span></span></li><li><span data-ttu-id="7235b-139">シンボル フォントは、すでにユーザーのコンピューターにキャッシュされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7235b-139">The symbol font should already be cached on the user's computer.</span></span> <span data-ttu-id="7235b-140">したがって、余分な帯域幅が使用されず、追加のネットワーク要求がないためにページの読み込みが遅くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7235b-140">Therefore, no extra bandwidth is used, and there are no additional network requests that might slow down page loads.</span></span></li><li><span data-ttu-id="7235b-141">色はテーマで制御できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-141">Colors can be controlled by themes.</span></span></li><li><span data-ttu-id="7235b-142">イメージは高 DPI ディスプレイで自動的に拡大/縮小されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-142">The images are automatically scaled on high-DPI displays.</span></span></li></ul>|<span data-ttu-id="7235b-143">限られた数のフレームワーク定義の記号を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-143">A limited number of framework-defined symbols is available.</span></span> |

### <a name="design-time"></a><span data-ttu-id="7235b-144">デザイン時間</span><span class="sxs-lookup"><span data-stu-id="7235b-144">Design time</span></span>
<span data-ttu-id="7235b-145"><strong>イメージの場所:</strong> 記号<strong>一般的な画像:</strong> &quot;個人&quot;</span><span class="sxs-lookup"><span data-stu-id="7235b-145"><strong>Image location:</strong> Symbol <strong>Typical image:</strong> &quot;Person&quot;</span></span>

### <a name="run-time"></a><span data-ttu-id="7235b-146">実行時間</span><span class="sxs-lookup"><span data-stu-id="7235b-146">Run time</span></span>
<span data-ttu-id="7235b-147">場合によっては、グリッド内の特定のレコードのイメージがない場合もありますが、イメージを配置する場所は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="7235b-147">Sometimes, you don't have an image for a particular record in a grid, but you don't want an empty space where the image should be.</span></span> <span data-ttu-id="7235b-148">次の例は、表示メソッドを使用してイメージ値をチェックし、代わりにプレースホルダー イメージを置換する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7235b-148">The following example shows how you can use a display method to check for an image value, and then substitute a placeholder image instead.</span></span>

```xpp
public display container customerImage()
{     
    ImageReference imgRef;
    container imgContainer = this.Image;
    if(imgContainer == connull())
    {
        // there is no image… the container is null
        // show a generic person outline image
        imgRef = ImageReference::constructForSymbol("Person");
        imgContainer = imgRef.pack();
    }
    return imgContainer;
}
```

## <a name="image-type-aot-resource"></a><span data-ttu-id="7235b-149">イメージの種類: AOT リソース</span><span class="sxs-lookup"><span data-stu-id="7235b-149">Image type: AOT Resource</span></span>

| <span data-ttu-id="7235b-150">プロ</span><span class="sxs-lookup"><span data-stu-id="7235b-150">Pros</span></span> | <span data-ttu-id="7235b-151">短所</span><span class="sxs-lookup"><span data-stu-id="7235b-151">Cons</span></span> |
|---|---|
| <span data-ttu-id="7235b-152">URL イメージ (次のセクションを参照) を使用するプロに加えて、AOT リソースが開発ツールでモデル化および管理されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-152">In addition to the pros of using URL images (see the next section), AOT resources are modeled and managed by the development tools.</span></span> | <span data-ttu-id="7235b-153">限られた数のフレームワーク定義の画像が使用できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-153">A   limited number of framework-defined images is available.</span></span> |

### <a name="design-time"></a><span data-ttu-id="7235b-154">デザイン時間</span><span class="sxs-lookup"><span data-stu-id="7235b-154">Design time</span></span>
<span data-ttu-id="7235b-155">| 新しいリソースを作成してからイメージをアプリケーション オブジェクト ツリー (AOT) リソースに保存するだけです。</span><span class="sxs-lookup"><span data-stu-id="7235b-155">| You just create a new resource and then save the image into the Application Object Tree (AOT) resource.</span></span> <span data-ttu-id="7235b-156">ページ上でイメージ コントロールをモデル化するときは、イメージ名ではなく、リソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="7235b-156">When you model your image control on a page, you specify the resource name, not the image name.</span></span> <span data-ttu-id="7235b-157">この方法は、通常、シンボル フォントに同等のものがないレガシ イメージ (アイコン) に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-157">This approach is typically used for legacy images (icons) that don’t have equivalents in the symbol font.</span></span> <span data-ttu-id="7235b-158"><strong>イメージの場所:</strong> AOTResource <strong>一般的な画像:</strong> &quot;ResourceMicrosoft Dynamics AX&quot; (.jpg をリソースに追加) |</span><span class="sxs-lookup"><span data-stu-id="7235b-158"><strong>Image location:</strong> AOTResource <strong>Typical image:</strong> &quot;ResourceMicrosoft Dynamics AX&quot; (a .jpg is added to resources) |</span></span>

### <a name="run-time"></a><span data-ttu-id="7235b-159">実行時間</span><span class="sxs-lookup"><span data-stu-id="7235b-159">Run time</span></span>

```xpp
public display container imageDataMethod()
{
    ImageReference imgClass =  
            ImageReference::constructForAotResource(
              "ResourceMicrosoft Dynamics AX");
    return imgClass.pack();
}
```

## <a name="image-type-url-image"></a><span data-ttu-id="7235b-160">イメージの種類: URL イメージ</span><span class="sxs-lookup"><span data-stu-id="7235b-160">Image type: URL Image</span></span>

| <span data-ttu-id="7235b-161">プロ</span><span class="sxs-lookup"><span data-stu-id="7235b-161">Pros</span></span> | <span data-ttu-id="7235b-162">短所</span><span class="sxs-lookup"><span data-stu-id="7235b-162">Cons</span></span> |
|---|---|
| <ul><li><span data-ttu-id="7235b-163">この方法は、web 上の任意の画像を参照する簡単な方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="7235b-163">This approach provides an easy way to reference any image anywhere on web.</span></span></li><li><span data-ttu-id="7235b-164">この方法は、フル カラー画像をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7235b-164">This approach supports full-color images.</span></span></li><li><span data-ttu-id="7235b-165">Web ブラウザーは、画像をホストするサーバーの設定に基づいて、画像をキャッシュできます。</span><span class="sxs-lookup"><span data-stu-id="7235b-165">The web browser can cache the image, based on the settings of the server that hosts the image.</span></span></li></ul> | <ul><li><span data-ttu-id="7235b-166">転送サイズはシンボルほど小さいわけではありませんが、妥当です。</span><span class="sxs-lookup"><span data-stu-id="7235b-166">The transfer size isn’t as small as it is for symbols, but it's reasonable.</span></span> <span data-ttu-id="7235b-167">URL は、画像を使用する各コントロールの文字列として送信されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-167">The URL is sent as a string for each control that uses the image.</span></span> <span data-ttu-id="7235b-168">ブラウザーは URL からイメージをダウンロードし、その時点から標準のブラウザー キャッシュ ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-168">The browser then downloads the image from the URL, and from that point, standard browser caching rules apply.</span></span></li><li><span data-ttu-id="7235b-169">CSS を使用してもイメージのテーマを簡単に提示することはできません。</span><span class="sxs-lookup"><span data-stu-id="7235b-169">You can’t easily theme the images by using CSS.</span></span></li><li><span data-ttu-id="7235b-170">URL がスケーラブル ベクター グラフィックス (SVG) ファイルを指していない場合、イメージは高 DPI ディスプレイでは自動的にスケーリングされません。</span><span class="sxs-lookup"><span data-stu-id="7235b-170">Unless the URL points to a Scalable Vector Graphics (SVG) file, the image isn't automatically scaled on high-DPI displays.</span></span></li></ul> |

| <span data-ttu-id="7235b-171">デザイン時間</span><span class="sxs-lookup"><span data-stu-id="7235b-171">Design time</span></span> | <span data-ttu-id="7235b-172">実行時間</span><span class="sxs-lookup"><span data-stu-id="7235b-172">Run time</span></span> |
|---|---|
| | <span data-ttu-id="7235b-173">次の例は、文字列に含まれる URL を使用するイメージを示しています。</span><span class="sxs-lookup"><span data-stu-id="7235b-173">The following example shows an image that uses a URL that is contained in a string.</span></span><br><pre><code>public display container imageDataMethod()<br>{<br>ImageReference imgClass = ImageReference::constructForUrl(this.ImageURL);<br>return imgClass.pack();<br>}</code></pre><br><span data-ttu-id="7235b-174">このコードは、小さな JavaScript Object Notation (JSON) メッセージをクライアントのコントロールに送信します。</span><span class="sxs-lookup"><span data-stu-id="7235b-174">This code sends a small JavaScript Object Notation (JSON) message to the control on the client.</span></span> <span data-ttu-id="7235b-175">このメッセージは、コントロールに画像を URL として扱い、ブラウザーに画像のダウンロード作業をさせるように指示します。</span><span class="sxs-lookup"><span data-stu-id="7235b-175">This message instructs the control to treat the image as a URL and let the browser do the work of downloading the image.</span></span> <span data-ttu-id="7235b-176">サーバーで発生しているダウンロードはありません。</span><span class="sxs-lookup"><span data-stu-id="7235b-176">No download occurs on the server.</span></span> <span data-ttu-id="7235b-177"><strong>データベース テーブルに画像 URL を格納する</strong>テーブル上にイメージ列のためのコンテナ フィールドを持つこともできます。</span><span class="sxs-lookup"><span data-stu-id="7235b-177"><strong>Storing an image URL in a database table</strong> You can also have a container field for the image column on your table.</span></span> <span data-ttu-id="7235b-178">以下の例を表すコードを使用して、<strong>ImageReference</strong> パックを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="7235b-178">You can then use code that resembles the following example to store the <strong>ImageReference</strong> pack.</span></span><br><pre><code>ImageReference imgClass;<br>CLIControls_ImageTable imgTable;<br>ttsbegin;<br>imgClass = ImageReference::constructForUrl(<br>    &quot;<br>    http://dynamics/PublishingImages/ERPLogos/DynamicsLogo.jpg&quot;);<br>imgTable.ImageField = imgClass.pack();<br>imgTable.insert();<br>ttscommit;</code></pre><span data-ttu-id="7235b-179">このコードにより、ユーザーのブラウザーは指定された URL からイメージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7235b-179">This code causes the user’s browser to download the image from the specified URL.</span></span> <span data-ttu-id="7235b-180">ImageReference の使用には間接費が発生しますが、このアプローチでは、バイナリデータ、URL、AOT リソース、シンボルから作成されたイメージを処理するために、単一のアプリケーション プログラミング インターフェイス (API) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-180">The use of ImageReference involves some overhead, but this approach lets you use a single application programming interface (API) to handle images that are created from binary data, URLs, AOT resources, or symbols.</span></span> <span data-ttu-id="7235b-181">データの行間でイメージの種類を組み合わせることもできます。</span><span class="sxs-lookup"><span data-stu-id="7235b-181">You can even mix and match image types between rows of data.</span></span>|

## <a name="image-type-binary-image"></a><span data-ttu-id="7235b-182">イメージの種類: バイナリ イメージ</span><span class="sxs-lookup"><span data-stu-id="7235b-182">Image type: Binary Image</span></span>

| <span data-ttu-id="7235b-183">プロ</span><span class="sxs-lookup"><span data-stu-id="7235b-183">Pros</span></span> | <span data-ttu-id="7235b-184">短所</span><span class="sxs-lookup"><span data-stu-id="7235b-184">Cons</span></span> |
|---|---|
| <span data-ttu-id="7235b-185">X++ の <strong>イメージ</strong> クラスが既に使用された場合、またはバイナリ イメージがデータベースに先に保存された場合、通常、この方法で移行が最も簡単に行われます。</span><span class="sxs-lookup"><span data-stu-id="7235b-185">Usually, this approach offers the easiest migration if the <strong>Image</strong> class in X++ was already used, or if binary images were previously stored in the database.</span></span> | <ul><li><span data-ttu-id="7235b-186">バイナリ イメージは文字列としてエンコードされ、相互作用の一部としてクライアントに送信されるため、この方法では転送サイズが最大になります。</span><span class="sxs-lookup"><span data-stu-id="7235b-186">This approach involves the largest transfer size, because the binary image is encoded as a string and sent to the client as part of the interaction.</span></span></li><li><span data-ttu-id="7235b-187">このブラウザーは、画像をキャッシュできません。</span><span class="sxs-lookup"><span data-stu-id="7235b-187">The browser can't cache the images.</span></span></li><li><span data-ttu-id="7235b-188">グリッドについては、複数の行が同じイメージを使用していても、バイナリ エンコード イメージがすべての行に対して送信されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-188">For a grid, the binary-encoded image is sent for every row, even if multiple rows use the same image.</span></span> <span data-ttu-id="7235b-189">したがって、このアプローチは、相互作用において非常に大きな転送サイズにつながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7235b-189">Therefore, this approach can lead to very large transfer sizes in the interactions.</span></span></li><li><span data-ttu-id="7235b-190">CSS を使用してもイメージのテーマを簡単に提示することはできません。</span><span class="sxs-lookup"><span data-stu-id="7235b-190">You can't easily theme the images by using CSS.</span></span></li><li><span data-ttu-id="7235b-191">イメージは高 DPI ディスプレイで自動的に拡大/縮小されません。</span><span class="sxs-lookup"><span data-stu-id="7235b-191">The images aren't automatically scaled on high-DPI displays.</span></span></li></ul> |

| <span data-ttu-id="7235b-192">デザイン時間</span><span class="sxs-lookup"><span data-stu-id="7235b-192">Design time</span></span> | <span data-ttu-id="7235b-193">実行時間</span><span class="sxs-lookup"><span data-stu-id="7235b-193">Run time</span></span> |
|---|---|
| <span data-ttu-id="7235b-194"><strong>データベース フィールドを使用</strong>この方法は、通常、従業員の写真や製品画像などのデータを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-194"><strong>Using a database field</strong> This approach is typically used to display data, such as employee pictures and product images.</span></span> <span data-ttu-id="7235b-195">フィールドに直接バインドするか、表示メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7235b-195">You can bind directly to a field, or you can use a display method.</span></span> <span data-ttu-id="7235b-196">データ ソース データ フィールドのデータ メソッド</span><span class="sxs-lookup"><span data-stu-id="7235b-196">Data Source Data Field Data Method</span></span> | <span data-ttu-id="7235b-197">通常、イメージはデータベースから読み込まれ、追加のコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7235b-197">Typically, the images are loaded from database, and no additional code is required.</span></span> <span data-ttu-id="7235b-198">データ メソッドで画像が管理されるケースでは、データ メソッドの例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7235b-198">For cases where the image is managed in a data method, see the data method examples.</span></span> |

## <a name="display-methods-and-images-three-return-types"></a><span data-ttu-id="7235b-199">メソッドとイメージを表示 (3 つの戻り値の型)</span><span class="sxs-lookup"><span data-stu-id="7235b-199">Display methods and images (three return types)</span></span>
<span data-ttu-id="7235b-200">画像タイプの表示メソッドを使用してグリッドに画像を表示するとき、フレームワークと連携する画像コントロールによって、次の 3 つの戻り値の型が認識されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-200">When you use a display method for an image type to show an image in a grid, three return types are understood by the image control that works with the framework.</span></span> <span data-ttu-id="7235b-201">3 つの戻り値の型すべてを使用して画像を表示できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-201">All three return types can be used to display an image.</span></span>

-   <span data-ttu-id="7235b-202">Int (imagelist 配列インデックス)</span><span class="sxs-lookup"><span data-stu-id="7235b-202">Int (imagelist array index)</span></span>
-   <span data-ttu-id="7235b-203">コンテナー (イメージ インスタンス)</span><span class="sxs-lookup"><span data-stu-id="7235b-203">Container (image instance)</span></span>
-   <span data-ttu-id="7235b-204">ResID (記号にマッピングされます)</span><span class="sxs-lookup"><span data-stu-id="7235b-204">ResID (which is mapped to a symbol)</span></span>

> [!NOTE]
> <span data-ttu-id="7235b-205">ResID および Int は、同じ戻り値の型です。</span><span class="sxs-lookup"><span data-stu-id="7235b-205">ResID and Int are the same return types.</span></span> <span data-ttu-id="7235b-206">画像コントロール インスタンスの**イメージ リスト** プロパティにインスタンス値が割り当てられている場合、表示メソッドの戻り値はイメージ リストへの配列インデックスと見なされます。</span><span class="sxs-lookup"><span data-stu-id="7235b-206">If the **imageList** property of the image control instance has been assigned an instance value, the display method return value is considered an array index into the imagelist.</span></span> <span data-ttu-id="7235b-207">**imageList** プロパティが **null** である場合、戻り値は、記号をレガシー ResID をマップするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7235b-207">If the **imageList** property is **null**, the return value is used to map a legacy ResID to a symbol.</span></span>

## <a name="images-in-a-grid-and-the-legacy-imagelist-collection"></a><span data-ttu-id="7235b-208">グリッドのイメージと旧式 ImageList コレクション</span><span class="sxs-lookup"><span data-stu-id="7235b-208">Images in a grid and the legacy ImageList collection</span></span>
<span data-ttu-id="7235b-209">AX 2012 およびそれ以前のバージョンにおいて、イメージを表示するための共通の使用パターンでは、リソースとしてイメージを格納、またはカーネルによって提供されるイメージ リソースを使用してから、実行時にそのイメージを抽出して、ImageList と呼ばれる再利用可能なコレクションに配置します。</span><span class="sxs-lookup"><span data-stu-id="7235b-209">In AX 2012 and earlier versions, a common use pattern for displaying images is to store an image as a resource or use a kernel-supplied image resource, and then at run time, extract that image and place it in a reusable collection that is known as an ImageList.</span></span> <span data-ttu-id="7235b-210">このガイダンスでは軽量の記号画像を使用します。</span><span class="sxs-lookup"><span data-stu-id="7235b-210">The guidance is to use lighter-weight symbol images.</span></span> <span data-ttu-id="7235b-211">すべてのレガシ コードは、記号を直接使用するように書き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="7235b-211">You should rewrite all legacy code so that it uses symbols directly.</span></span> <span data-ttu-id="7235b-212">ImageList コレクションを使用するすべてのコードを置換する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="7235b-212">You should also replace all code that uses the ImageList collection.</span></span> <span data-ttu-id="7235b-213">これらの変更を行わない場合は、旧式 ImageList コレクションを使用すると、もはや存在しない埋め込み (カーネル) のリソースに依存するため、イメージが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="7235b-213">If you don't make these changes, the legacy ImageList collection won't display images, because use of this collection relies on embedded (kernel) resources that no longer exist.</span></span> <span data-ttu-id="7235b-214">したがって、更新されるまでレガシー コードをサポートするために、ImageList コレクションは埋め込みリソースの ResID を新しいフォント ベースのシンボルにマップし、ImageList コレクションを使用するコードが引き続き実行され、イメージが提供されるようにします。</span><span class="sxs-lookup"><span data-stu-id="7235b-214">Therefore, to support legacy code until it can be updated, the ImageList collection maps the ResID for an embedded resource to a new font-based symbol to help guarantee that any code that uses the ImageList collection will continue to run and provide an image.</span></span>

## <a name="using-the-imagelist-property-for-backward-compatibility"></a><span data-ttu-id="7235b-215">下位互換性のための imageList プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="7235b-215">Using the imageList property for backward compatibility</span></span>
<span data-ttu-id="7235b-216">イメージ コントロールには **imageList** という名前のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7235b-216">An image control has a property that is named **imageList**.</span></span> <span data-ttu-id="7235b-217">このプロパティに ImageList コレクションのインスタンスに渡します。</span><span class="sxs-lookup"><span data-stu-id="7235b-217">You pass in an instance of the ImageList collection to this property.</span></span> <span data-ttu-id="7235b-218">この方法で、イメージは配列番号で選択したイメージの配列です。</span><span class="sxs-lookup"><span data-stu-id="7235b-218">In this way, the image is an array of images that you select via the array number.</span></span>

```xpp
public void init()
{
    int imgCnt;
        
    // create an imagelist instance
    Imagelist imageList = new ImageList(ImageList::smallIconWidth(), Imagelist::smallIconHeight());
        
    super();
        
    // add images to the instance (return value is not needed)
    // Note that a legacy ResID is used in the new Image contstructor. 
    // This is a compatibility mapping of resource to symbol.
    imgCnt = imagelist.add(new Image(#ImageInfo));
    imgCnt = imagelist.add(new Image(#ImageWarning));
    imgCnt = imagelist.add(new Image(#ImageError));
        
    // pass the image list instance to the control
    ImageListDM.imageList(imageList);
}
    
// at runtime, select the image you want to show: when the control has an imagelist instance, 
// this int value is used to index into that array
public display int imageListDataMethod()
{
    int imgCnt = imageCnt mod 3;
    imageCnt++;
    return imgCnt;
}
    
/*
    Note: The legacy image resource ID's #ImageInfo, #ImageWarning, #ImageError are 
    mapped from the legacy resource id to a symbol name in the X++
    class ImageLoader
*/
```

## <a name="display-method-that-returns-an-imageres-legacy-image-resource-id"></a><span data-ttu-id="7235b-219">ImageRes を返すメソッドを表示 (レガシ イメージ リソース ID)</span><span class="sxs-lookup"><span data-stu-id="7235b-219">Display method that returns an ImageRes (legacy image resource ID)</span></span>

```xpp
// this is an example of backward compatibility the use of ImageRes will become obsolete
display ImageRes checkIfError(HRMCompEventEmpl _hrmCompEventEmpl)
{
    if (!_hrmCompEventEmpl.RecId)
    {
        return 0;
    }       
    if (_hrmCompEventEmpl.Status == HRMCompEventEmplStatus::Ignore   ||
        _hrmCompEventEmpl.Status == HRMCompEventEmplStatus::Approved ||
        _hrmCompEventEmpl.Status == HRMCompEventEmplStatus::Loaded)
    {
        return 0;
    }
    else
    {
        if (_hrmCompEventEmpl.ErrorStatus == HRMCompEventErrorStatus::Error)
        {
            return #ImageError;
        }
        if (_hrmCompEventEmpl.ErrorStatus == HRMCompEventErrorStatus::Warning)
        {
            return #ImageWarning;
        }
        if (_hrmCompEventEmpl.ErrorStatus == HRMCompEventErrorStatus::Info)
        {
            return #ImageInfo;
        }
    }      
    return 0;
}
```

## <a name="display-method-that-returns-a-container"></a><span data-ttu-id="7235b-220">コンテナーを返すメソッドを表示</span><span class="sxs-lookup"><span data-stu-id="7235b-220">Display method that returns a container</span></span>

```xpp
public display container checkIfError(HRMCompEventEmpl _hrmCompEventEmpl)
{
    ImageReference  imageReference;
    container       imageContainer;
    if (_hrmCompEventEmpl.RecId && _hrmCompEventEmpl.Status == HRMCompEventEmplStatus::Created)
    {
        switch (_hrmCompEventEmpl.ErrorStatus)
        {
            case HRMCompEventErrorStatus::Error:
                imageReference = ImageReference::constructForSymbol('Error');
                break;
            case HRMCompEventErrorStatus::Warning:
                imageReference = ImageReference::constructForSymbol('Warning');
                break;
            case HRMCompEventErrorStatus::Info:
                imageReference = ImageReference::constructForSymbol('Info');
                break;
        }
    }
    if (imageReference)
    {
        imageContainer = imageReference.pack();
    }
    return imageContainer;
}
```

## <a name="obtaining-and-displaying-an-image-from-the-user-by-using-file-upload"></a><span data-ttu-id="7235b-221">ファイルのアップロードを使用して、ユーザーからの画像を取得し表示</span><span class="sxs-lookup"><span data-stu-id="7235b-221">Obtaining and displaying an image from the user by using file upload</span></span>
<span data-ttu-id="7235b-222">イメージ コントロールと **FileUpload** ボタンがあるページをモデル化します。</span><span class="sxs-lookup"><span data-stu-id="7235b-222">Model a page that has an image control and a **FileUpload** button.</span></span>

```xpp
// model a new FileUpload control (style=minimal)
// class declaration
FileUpload uploadControl;
    
// form init() create a callback event handler to be notified when upload is complete
public void init()
{
    //when uploading an image, this method is called upon completion.
    uploadControl = FileUpload1;
    uploadControl.notifyUploadCompleted +=  eventhandler(this.UploadCompleted);
}
    
// form close() release the callback event handler
public void close()
{
    // when the form closes, release the eventhandler for file upload callback
    //  FileUpload uploadControl;
    super();
    //  uploadControl = FileUpload1;
    uploadControl.notifyUploadCompleted -=  eventhandler(this.UploadCompleted);
}
    
// when the upload completes, grab the image and store it in the database
/// <summary> 
/// This method is called by the file upload mechanism, when the upload completes
/// </summary>
public void UploadCompleted()
{
    Binary binaryImage;
    System.Net.WebClient webClient;
    System.IO.MemoryStream stream;
    String255 myUrl;
    if(uploadControl.uploadSuccess())
    {
        InteropPermission perm = new InteropPermission(InteropKind::ClrInterop);
        perm.assert();
            
        // BP Deviation Documented
        webClient = new System.Net.WebClient();
            
        // BP Deviation Documented
        // if success, downloadURL contains the path to the Azure blob location for the file
        stream = new System.IO.MemoryStream(webClient.DownloadData(uploadControl.downloadUrl()));
            
        // grab the data and assign to the image field
        binaryImage = Binary::constructFromMemoryStream(stream);
            
        // assign to the database field (type=container)
        FMVehicleModel.Image = binaryImage.getContainer();
            
        CodeAccessPermission::revertAssert();
    }
}
```

## <a name="example-of-in-memory-bitmap-manipulation"></a><span data-ttu-id="7235b-223">メモリ内ビットマップ操作の例</span><span class="sxs-lookup"><span data-stu-id="7235b-223">Example of in-memory bitmap manipulation</span></span>
<span data-ttu-id="7235b-224">この例では、最初からイメージが作成されています。</span><span class="sxs-lookup"><span data-stu-id="7235b-224">In this example, an image is created from scratch.</span></span> <span data-ttu-id="7235b-225">ただし、開発者は代替ソースからビットマップを読み込むこともでき、必要に応じて画像を操作します (たとえば、クロッピング、ストレッチ、またはサイズ変更により、または透過度を変更することにより)。</span><span class="sxs-lookup"><span data-stu-id="7235b-225">However, developers can also load a bitmap from an alternative source and then manipulate the image as desired (for example, by cropping, stretching, or resizing, or by changing the opacity).</span></span> <span data-ttu-id="7235b-226">任意の操作が完了した後、開発者はイメージ コントロールを使用して画像を表示したり、データ ソース フィールドを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="7235b-226">After any manipulation is completed, the developers can display the image by using the image control, or they can assign it to a data source field.</span></span>

```xpp
public void clicked()
{
    Binary binaryImage;
    Image  image;
    int x,y;
        
    super();
        
    InteropPermission perm = new InteropPermission(InteropKind::ClrInterop);
    perm.assert();
        
    /* 
    In this example, we’ll create a bitmap programmatically, we’ll use a memory
    Stream o’bytes to then convert to the container format the image control expects.
    */
    System.Drawing.Bitmap bitmap = new System.Drawing.Bitmap(100,100);
    System.IO.MemoryStream myStream = new System.IO.MemoryStream();
        
    // draw some stuff (or load a bitmap from an alternative source)
    for( x=0; x < bitmap.Height; ++x)
    {
        for( y=0; y< bitmap.Width; ++y)
        {
            bitmap.SetPixel(x,y,System.Drawing.Color::White);
        }
    }
        
    for(x=0; x < bitmap.Height; ++x)
    {
        bitmap.SetPixel(x,x, System.Drawing.Color::Red);
    }
        
    // move our bitmap to an in memory stream
    bitmap.Save(myStream, System.Drawing.Imaging.ImageFormat::Bmp);
        
    // stream goes to raw binary
    binaryImage = Binary::constructFromMemoryStream(myStream);
        
    // create a blank image and copy our binary data to the image format
    image = new Image();
    image.setData(binaryImage.getContainer());
        
    // copy the image data to the image control
    MyImage.image(image);
        
    // alternatively, skip the image conversion step and assign directly to the data field
    binaryImage = Binary::constructFromMemoryStream(myStream);
        
    // assign to the database field (type=container)
    datafield.Image = binaryImage.getContainer();
        
    CodeAccessPermission::revertAssert();
}
```

## <a name="additional-examples-url-binary-and-symbol"></a><span data-ttu-id="7235b-227">追加の例 (URL、バイナリ、記号)</span><span class="sxs-lookup"><span data-stu-id="7235b-227">Additional examples (URL, binary, and symbol)</span></span>
<span data-ttu-id="7235b-228">次のテーブルでは、イメージ クラスと FormImageControl の 2 つの概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="7235b-228">The following table explains two concepts: Image Class and FormImageControl.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7235b-229">イメージ クラス</span><span class="sxs-lookup"><span data-stu-id="7235b-229">Image Class</span></span></td>
<td><span data-ttu-id="7235b-230">このクラスは、画像の実行時表示です。</span><span class="sxs-lookup"><span data-stu-id="7235b-230">This class is a run-time representation of an image.</span></span></td>
<td><span data-ttu-id="7235b-231">4 つのコンストラクター:</span><span class="sxs-lookup"><span data-stu-id="7235b-231">Four constructors:</span></span>
<ul>
<li><span data-ttu-id="7235b-232">Image::ConstructBinary(INT64Encode);</span><span class="sxs-lookup"><span data-stu-id="7235b-232">Image::ConstructBinary(INT64Encode);</span></span></li>
<li><span data-ttu-id="7235b-233">Image::ConstructSymbol(SymbolName);</span><span class="sxs-lookup"><span data-stu-id="7235b-233">Image::ConstructSymbol(SymbolName);</span></span></li>
<li><span data-ttu-id="7235b-234">Image::ConstructURL(URL);</span><span class="sxs-lookup"><span data-stu-id="7235b-234">Image::ConstructURL(URL);</span></span></li>
<li><span data-ttu-id="7235b-235">Image::Construct(ResourceName);</span><span class="sxs-lookup"><span data-stu-id="7235b-235">Image::Construct(ResourceName);</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7235b-236">FormImageControl</span><span class="sxs-lookup"><span data-stu-id="7235b-236">FormImageControl</span></span></td>
<td><span data-ttu-id="7235b-237">このコントロールを使用して、実行時に画像を追加できます。</span><span class="sxs-lookup"><span data-stu-id="7235b-237">This control is used to add an image at run time.</span></span></td>
<td><span data-ttu-id="7235b-238">.image(new image());</span><span class="sxs-lookup"><span data-stu-id="7235b-238">.image(new image());</span></span></td>
</tr>
</tbody>
</table>

## <a name="using-a-display-method-to-show-an-image-from-a-url-string"></a><span data-ttu-id="7235b-239">表示メソッドを使用して URL 文字列から画像を表示</span><span class="sxs-lookup"><span data-stu-id="7235b-239">Using a display method to show an image from a URL string</span></span>
<span data-ttu-id="7235b-240">この例では、表示メソッドを使用してイメージ コントロールが期待している形式に URL を含む文字列を変換します。</span><span class="sxs-lookup"><span data-stu-id="7235b-240">In this example, a display method is used to translate a string that contains a URL to the format that the image control expects.</span></span>

```xpp
public display container imageDataMethod()
{
    ImageReference imgClass = ImageReference::constructForUrl(this.ImageURL);
    return imgClass.pack();
}
```

<span data-ttu-id="7235b-241">このコードは、小さな JSON メッセージをクライアントのコントロールに送信します。</span><span class="sxs-lookup"><span data-stu-id="7235b-241">This code sends a small JSON message to the control on the client.</span></span> <span data-ttu-id="7235b-242">このメッセージは、コントロールに画像を URL として扱い、ブラウザーに画像のダウンロード作業をさせるように指示します。</span><span class="sxs-lookup"><span data-stu-id="7235b-242">This message instructs the control to treat the image as a URL and let the browser do the work of downloading the image.</span></span> <span data-ttu-id="7235b-243">サーバーで発生しているダウンロードはありません。</span><span class="sxs-lookup"><span data-stu-id="7235b-243">No download occurs on the server.</span></span>

## <a name="using-a-display-method-to-show-a-blank-image"></a><span data-ttu-id="7235b-244">表示メソッドを使用して空白の画像を表示</span><span class="sxs-lookup"><span data-stu-id="7235b-244">Using a display method to show a blank image</span></span>
<span data-ttu-id="7235b-245">グリッド内の特定のレコードのイメージがない場合もありますが、イメージを配置する場所は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="7235b-245">There might be times when you have no image for a particular record in a grid, but you don't want an empty space where the image should be.</span></span> <span data-ttu-id="7235b-246">この例では、表示方法を使用してイメージ値をチェックし、代わりにプレースホルダー イメージを置換する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7235b-246">This example shows how you can use a display method to check for an image value and then substitute a placeholder image instead.</span></span>

```xpp
public display container customerImage()
{
    ImageReference imgRef;
    container imgContainer = this.Image;
    if(imgContainer == connull())  // there is no image… the container is null
    {
        imgRef = ImageReference::constructForSymbol("Person");  // show a generic person outline image
        imgContainer = imgRef.pack();
    }
    return imgContainer;
}
public display container statusImageDataMethod()
{
    ImageReference statusImage;
    if (this.Status == NoYes::Yes)
    {
        statusImage = ImageReference::constructForSymbol("Accept");
    }
    else
    {
        statusImage = ImageReference::constructForSymbol("Cancel");
    }
    return statusImage.pack();
}
```

## <a name="taking-an-image-url-and-storing-the-image-in-table"></a><span data-ttu-id="7235b-247">画像の URL を取得し、テーブルに画像を格納</span><span class="sxs-lookup"><span data-stu-id="7235b-247">Taking an image URL and storing the image in table</span></span>
<span data-ttu-id="7235b-248">テーブル上にはイメージ列のためのコンテナ フィールドがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="7235b-248">You can have a container field for the image column on your table.</span></span> <span data-ttu-id="7235b-249">以下の例を表すコードを使用して、**ImageReference** パックを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="7235b-249">You can then use code that resembles the following example to store the **ImageReference** pack.</span></span>

```xpp
ImageReference imgClass;
CLIControls_ImageTable imgTable;
ttsbegin;
imgClass = ImageReference::constructForUrl(
    "http://dynamics/PublishingImages/ERPLogos/DynamicsLogo.jpg");
imgTable.ImageField = imgClass.pack();
imgTable.insert();
ttscommit;
```

<span data-ttu-id="7235b-250">「表示メソッドを使用して URL 文字列から画像を表示」のセクションに記載されている表示メソッドと同様に、このコードを使用するとユーザーのブラウザーは指定した URL から画像をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7235b-250">Like the display method that is described in the "Using a display method to show an image from a URL string" section, this code causes the user's browser to download the image from the specified URL.</span></span> <span data-ttu-id="7235b-251">この方法はいくらかの間接費を伴いますが、バイナリ データ、URL、AOT リソースまたは記号から作成された画像を処理するために単一の API を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7235b-251">Although this approach involves some overhead, you can use a single API to handle images that are created from binary data, URLs, AOT resources, or symbols.</span></span> <span data-ttu-id="7235b-252">データの行間でイメージの種類を組み合わせることもできます。</span><span class="sxs-lookup"><span data-stu-id="7235b-252">You can even mix and match image types between rows of data.</span></span>


