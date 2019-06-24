---
title: ページ上またはグリッド内の画像
description: このトピックでは、画像をページまたはグリッドに表示する手順について説明します。 このトピックでは、イメージの使用方法のいくつかについての背景と、使用される API についても説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 55871
ms.assetid: 58e6476b-c29f-46c4-8866-78ca4ab3c0bc
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43257e6ed0c8a7ca74a7cddc685e6113352a1c03
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570986"
---
# <a name="images-on-a-page-or-in-a-grid"></a>ページ上またはグリッド内の画像

[!include [banner](../includes/banner.md)]

このトピックでは、画像をページまたはグリッドに表示する手順について説明します。 このトピックでは、イメージの使用方法のいくつかについての背景と、使用される API についても説明します。  

**注記:** アクセシビリティのために、画像を使用して状態を示したり、データを表示するときには、その画像が表す値または状態を説明するツールヒント、拡張プレビュー、ラベル、またはその他のテキスト形式表記が添付されていなければなりません。 

Microsoft Dynamics AX 2012 とは異なり、Microsoft Dynamics 365 for Finance and Operations ではイメージに埋め込みリソースを使用しません。 代わりに、ライトウェイト記号を使用します。 新しいイメージ コントロールをサポートするために、コーディング パターンがわずかに変更されました。 

ImageList 使用により、ランタイムは古い **ImageID** 値を受け入れて記号にマップし、既存のコードは引き続き動作できるようにします。

**注記:** 場合によっては、ランタイム マッピング後もイメージが存在せず、この動作は意図的です。 

AX 2012 は、ステータスを示すためにグリッド列で画像を表示します。 これらの画像は、利用できなくなった埋め込みリソースから取得されることがありました。 

AX 2012は、画像の次の記憶域オプションが用意されています。

-   画像がカーネル自体の一部として提供される埋め込みリソース
-   Application Object Server (AOS) リソースは開発者または独立系ソフトウェア ベンダー (ISV) が独自のイメージ リソースを追加できます。
-   実行時に開発者または ISV が画像を読み込むファイルの場所
-   ビットマップとして保存されているデータベース フィールド

Finance and Operations は、画像用に次の記憶域オプションを提供します。

-   AOS リソースは開発者や ISV が独自のイメージ リソースを追加できます。
-   実行時に開発者または ISVs が画像を読み込む URL の場所
-   コンテナーとして保存されているデータベース フィールドです。
-   画像がフォントの名前でレンダリングされる記号フォント

Finance and Operations では、埋め込みリソース (カーネル リソース) が破棄されました。 

AOS リソースとして保存されるイメージは、ユーザー データに分類されていないイメージを使用でき、お使いのアプリケーションと共に使用できます。 

**注記:** UX が使用を承認したレガシ埋め込みリソース イメージがある場合、それらの埋め込みイメージを手動で AOS リソースに転送して使用できます。 

一般的な Web アプリケーションは、Internet Information Services (IIS) サーバー上の画像のコレクションを管理し、画像の URL を提供します。 この方法はサポートされていますが、非常に多く使用されるとは考えていません。 代わりに、記号フォントをイメージ ソースとして使用することを期待します。 

もちろん、アプリケーション ロジックは、許可された厳密な従業員の写真、製品画像など、データベースに画像を保管し、この方法は、ファースト クラスの経験です。 

記号フォントは、最もパフォーマンスが高く、スケーラブルな画像形式です。 ほとんどのアプリケーションのユース ケース (グリッドの行ごとのステータスやボタンの画像など) に記号フォントの文字の使用を考えています。 

記号フォントで利用できる記号の一覧については、[記号フォント](symbol-font.md) を参照してください。

## <a name="image-type-symbol"></a>イメージの種類: シンボル

| プロ | 短所 |
|---|---|
| <ul><li>通常、記号フォントは、クライアントに送られる最小のペイロードです。</li><li>カスケード スタイル シート (CSS) を使用することにより、画像を簡単にカスタマイズすることができます。</li><li>シンボル フォントは、すでにユーザーのコンピューターにキャッシュされている必要があります。 したがって、余分な帯域幅が使用されず、追加のネットワーク要求がないためにページの読み込みが遅くなる可能性があります。</li><li>色はテーマで制御できます。</li><li>イメージは高 DPI ディスプレイで自動的に拡大/縮小されます。</li></ul>|限られた数のフレームワーク定義の記号を使用できます。 |

### <a name="design-time"></a>デザイン時間
<strong>イメージの場所:</strong> 記号<strong>一般的な画像:</strong> &quot;個人&quot;

### <a name="run-time"></a>実行時間
場合によっては、グリッド内の特定のレコードのイメージがない場合もありますが、イメージを配置する場所は空ではありません。 次の例は、表示メソッドを使用してイメージ値をチェックし、代わりにプレースホルダー イメージを置換する方法を示しています。

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


## <a name="image-type-aot-resource"></a>イメージの種類: AOT リソース

| プロ | 短所 |
|---|---|
| URL イメージ (次のセクションを参照) を使用するプロに加えて、AOT リソースが開発ツールでモデル化および管理されます。 | 限られた数のフレームワーク定義の画像が使用できます。 |

### <a name="design-time"></a>デザイン時間
| 新しいリソースを作成してからイメージをアプリケーション オブジェクト ツリー (AOT) リソースに保存するだけです。 ページ上でイメージ コントロールをモデル化するときは、イメージ名ではなく、リソース名を指定します。 この方法は、通常、シンボル フォントに同等のものがないレガシ イメージ (アイコン) に使用されます。 <strong>イメージの場所:</strong> AOTResource <strong>一般的な画像:</strong> &quot;ResourceMicrosoft Dynamics AX&quot; (.jpg をリソースに追加) |

### <a name="run-time"></a>実行時間

    public display container imageDataMethod()
    {
        ImageReference imgClass =  
              ImageReference::constructForAotResource(
                  "ResourceMicrosoft Dynamics AX");
        return imgClass.pack();
    }

## <a name="image-type-url-image"></a>イメージの種類: URL イメージ

| プロ | 短所 |
|---|---|
| <ul><li>この方法は、web 上の任意の画像を参照する簡単な方法を説明します。</li><li>この方法は、フル カラー画像をサポートします。</li><li>Web ブラウザーは、画像をホストするサーバーの設定に基づいて、画像をキャッシュできます。</li></ul> | <ul><li>転送サイズはシンボルほど小さいわけではありませんが、妥当です。 URL は、画像を使用する各コントロールの文字列として送信されます。 ブラウザーは URL からイメージをダウンロードし、その時点から標準のブラウザー キャッシュ ルールが適用されます。</li><li>CSS を使用してもイメージのテーマを簡単に提示することはできません。</li><li>URL がスケーラブル ベクター グラフィックス (SVG) ファイルを指していない場合、イメージは高 DPI ディスプレイでは自動的にスケーリングされません。</li></ul> |

| デザイン時間 | 実行時間 |
|---|---|
| | 次の例は、文字列に含まれる URL を使用するイメージを示しています。<br><pre><code>public display container imageDataMethod()<br>{<br>ImageReference imgClass = ImageReference::constructForUrl(this.ImageURL);<br>return imgClass.pack();<br>}</code></pre><br>このコードは、小さな JavaScript Object Notation (JSON) メッセージをクライアントのコントロールに送信します。 このメッセージは、コントロールに画像を URL として扱い、ブラウザーに画像のダウンロード作業をさせるように指示します。 サーバーで発生しているダウンロードはありません。 <strong>データベース テーブルに画像 URL を格納する</strong>テーブル上にイメージ列のためのコンテナ フィールドを持つこともできます。 以下の例を表すコードを使用して、<strong>ImageReference</strong> パックを保存することができます。<br><pre><code>ImageReference imgClass;<br>CLIControls_ImageTable imgTable;<br>ttsbegin;<br>imgClass = ImageReference::constructForUrl(<br>    &quot;<br>    http://dynamics/PublishingImages/ERPLogos/DynamicsLogo.jpg&quot;);<br>imgTable.ImageField = imgClass.pack();<br>imgTable.insert();<br>ttscommit;</code></pre>このコードにより、ユーザーのブラウザーは指定された URL からイメージをダウンロードします。 ImageReference の使用には間接費が発生しますが、このアプローチでは、バイナリデータ、URL、AOT リソース、シンボルから作成されたイメージを処理するために、単一のアプリケーション プログラミング インターフェイス (API) を使用できます。 データの行間でイメージの種類を組み合わせることもできます。|

## <a name="image-type-binary-image"></a>イメージの種類: バイナリ イメージ

| プロ | 短所 |
|---|---|
| X++ の <strong>イメージ</strong> クラスが既に使用された場合、またはバイナリ イメージがデータベースに先に保存された場合、通常、この方法で移行が最も簡単に行われます。 | <ul><li>バイナリ イメージは文字列としてエンコードされ、相互作用の一部としてクライアントに送信されるため、この方法では転送サイズが最大になります。</li><li>このブラウザーは、画像をキャッシュできません。</li><li>グリッドについては、複数の行が同じイメージを使用していても、バイナリ エンコード イメージがすべての行に対して送信されます。 したがって、このアプローチは、相互作用において非常に大きな転送サイズにつながる可能性があります。</li><li>CSS を使用してもイメージのテーマを簡単に提示することはできません。</li><li>イメージは高 DPI ディスプレイで自動的に拡大/縮小されません。</li></ul> |

| デザイン時間 | 実行時間 |
|---|---|
| <strong>データベース フィールドを使用</strong>この方法は、通常、従業員の写真や製品画像などのデータを表示するために使用されます。 フィールドに直接バインドするか、表示メソッドを使用することができます。 データ ソース データ フィールドのデータ メソッド | 通常、イメージはデータベースから読み込まれ、追加のコードは必要ありません。 データ メソッドで画像が管理されるケースでは、データ メソッドの例を参照してください。 |

## <a name="display-methods-and-images-three-return-types"></a>メソッドとイメージを表示 (3 つの戻り値の型)
画像タイプの表示メソッドを使用してグリッドに画像を表示するとき、フレームワークと連携する画像コントロールによって、次の 3 つの戻り値の型が認識されます。 3 つの戻り値の型すべてを使用して画像を表示できます。

-   Int (imagelist 配列インデックス)
-   コンテナー (イメージ インスタンス)
-   ResID (記号にマッピングされます)

**注記:** ResID および Int は、同じ戻り値の型です。 画像コントロール インスタンスの**イメージ リスト** プロパティにインスタンス値が割り当てられている場合、表示メソッドの戻り値はイメージ リストへの配列インデックスと見なされます。 **imageList** プロパティが **null** である場合、戻り値は、記号をレガシー ResID をマップするために使用されます。

## <a name="images-in-a-grid-and-the-legacy-imagelist-collection"></a>グリッドのイメージと旧式 ImageList コレクション
AX 2012 およびそれ以前のバージョンにおいて、イメージを表示するための共通の使用パターンでは、リソースとしてイメージを格納、またはカーネルによって提供されるイメージ リソースを使用してから、実行時にそのイメージを抽出して、ImageList と呼ばれる再利用可能なコレクションに配置します。 このガイダンスでは軽量の記号画像を使用します。 すべてのレガシ コードは、記号を直接使用するように書き換える必要があります。 ImageList コレクションを使用するすべてのコードを置換する必要もあります。 これらの変更を行わない場合は、旧式 ImageList コレクションを使用すると、もはや存在しない埋め込み (カーネル) のリソースに依存するため、イメージが表示されなくなります。 したがって、更新されるまでレガシー コードをサポートするために、ImageList コレクションは埋め込みリソースの ResID を新しいフォント ベースのシンボルにマップし、ImageList コレクションを使用するコードが引き続き実行され、イメージが提供されるようにします。

## <a name="using-the-imagelist-property-for-backward-compatibility"></a>下位互換性のための imageList プロパティの使用
イメージ コントロールには **imageList** という名前のプロパティがあります。 このプロパティに ImageList コレクションのインスタンスに渡します。 この方法で、イメージは配列番号で選択したイメージの配列です。

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

## <a name="display-method-that-returns-an-imageres-legacy-image-resource-id"></a>ImageRes を返すメソッドを表示 (レガシ イメージ リソース ID)
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

## <a name="display-method-that-returns-a-container"></a>コンテナーを返すメソッドを表示
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

## <a name="obtaining-and-displaying-an-image-from-the-user-by-using-file-upload"></a>ファイルのアップロードを使用して、ユーザーからの画像を取得し表示
イメージ コントロールと **FileUpload** ボタンがあるページをモデル化します。

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

## <a name="example-of-in-memory-bitmap-manipulation"></a>メモリ内ビットマップ操作の例
この例では、最初からイメージが作成されています。 ただし、開発者は代替ソースからビットマップを読み込むこともでき、必要に応じて画像を操作します (たとえば、クロッピング、ストレッチ、またはサイズ変更により、または透過度を変更することにより)。 任意の操作が完了した後、開発者はイメージ コントロールを使用して画像を表示したり、データ ソース フィールドを割り当てることができます。

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

## <a name="additional-examples-url-binary-and-symbol"></a>追加の例 (URL、バイナリ、記号)
次のテーブルでは、イメージ クラスと FormImageControl の 2 つの概念について説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>イメージ クラス</td>
<td>このクラスは、画像の実行時表示です。</td>
<td>4 つのコンストラクター:
<ul>
<li>Image::ConstructBinary(INT64Encode);</li>
<li>Image::ConstructSymbol(SymbolName);</li>
<li>Image::ConstructURL(URL);</li>
<li>Image::Construct(ResourceName);</li>
</ul></td>
</tr>
<tr class="even">
<td>FormImageControl</td>
<td>このコントロールを使用して、実行時に画像を追加できます。</td>
<td>.image(new image());</td>
</tr>
</tbody>
</table>

## <a name="using-a-display-method-to-show-an-image-from-a-url-string"></a>表示メソッドを使用して URL 文字列から画像を表示
この例では、表示メソッドを使用してイメージ コントロールが期待している形式に URL を含む文字列を変換します。

    public display container imageDataMethod()
    {
        ImageReference imgClass = ImageReference::constructForUrl(this.ImageURL);
        return imgClass.pack();
    }

このコードは、小さな JSON メッセージをクライアントのコントロールに送信します。 このメッセージは、コントロールに画像を URL として扱い、ブラウザーに画像のダウンロード作業をさせるように指示します。 サーバーで発生しているダウンロードはありません。

## <a name="using-a-display-method-to-show-a-blank-image"></a>表示メソッドを使用して空白の画像を表示
グリッド内の特定のレコードのイメージがない場合もありますが、イメージを配置する場所は空ではありません。 この例では、表示方法を使用してイメージ値をチェックし、代わりにプレースホルダー イメージを置換する方法を示します。

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

## <a name="taking-an-image-url-and-storing-the-image-in-table"></a>画像の URL を取得し、テーブルに画像を格納
テーブル上にはイメージ列のためのコンテナ フィールドがある場合があります。 以下の例を表すコードを使用して、**ImageReference** パックを保存することができます。

    ImageReference imgClass;
    CLIControls_ImageTable imgTable;
    ttsbegin;
    imgClass = ImageReference::constructForUrl(
        "http://dynamics/PublishingImages/ERPLogos/DynamicsLogo.jpg");
    imgTable.ImageField = imgClass.pack();
    imgTable.insert();
    ttscommit;

「表示メソッドを使用して URL 文字列から画像を表示」のセクションに記載されている表示メソッドと同様に、このコードを使用するとユーザーのブラウザーは指定した URL から画像をダウンロードします。 この方法はいくらかの間接費を伴いますが、バイナリ データ、URL、AOT リソースまたは記号から作成された画像を処理するために単一の API を使用することができます。 データの行間でイメージの種類を組み合わせることもできます。


