---
title: ビジネス ドキュメントのカスタム デザインを作成する
description: この記事では、純粋な拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを作成する方法について説明します。
author: RichdiMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.custom:
- "266574"
ms.assetid: fba7faa3-716b-4adf-ab3e-8573f3614894
ms.openlocfilehash: b7223c15f33a61ff2f71eff36352a4294df3797c
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205920"
---
# <a name="create-custom-designs-for-business-documents"></a>ビジネス ドキュメントのカスタム デザインを作成する

[!include [banner](../includes/banner.md)]

この記事では、純粋な拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを作成する方法について説明します。

Microsoft Dynamics 365 Finance には、カスタム ソリューションをサポートするためのツールの拡張セットが含まれています。 この記事では、純粋な拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを作成する手順について説明します。 カスタム レポート デザインをアプリケーション ドキュメントのインスタンスに関連付けるには、この記事で後述する手順に従います。 完了したら、ユーザーは印刷管理設定を構成して、 該当するときはいつでも、カスタムのデザインを選択できます。 次の図は、一般的なアプリケーションのカスタマイズを示しています。

[![extendingprintmgt。](./media/extendingprintmgt1.png)](./media/extendingprintmgt1.png)

## <a name="whats-important-to-know"></a>知っている必要がある重要なこと
このソリューションを適用する前に注意すべき重要な点を次に示します。

- 印刷管理設定は、有効な法人に適用されます。 カスタム デザインは、1 つ以上の印刷管理設定を関連付けることができます。
- 標準レポート デザインは、カスタム ソリューションと共に引き続き使用できます。 印刷管理設定を使用して、トランザクションの詳細に基づいて適切なデザインを選択します。
- カスタム ビジネス プロセスのビジネス ドキュメントを導入する場合は、多くの作業が必要です。 カスタム ビジネス ドキュメント ソリューションの作成方法の詳細については、[印刷管理の統合ガイド](https://www.microsoft.com/download/details.aspx?id=36049) を参照してください。

## <a name="customize-a-business-document"></a>ビジネス ドキュメントのカスタマイズ
次のチュートリアルでは、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを導入し、次に印刷管理を使用して新しいデザインを選択するプロセスを示します。 このソリューションには、Application Suite モデルの一部として標準アプリケーションで提供される **販売の確認** レポートのカスタム設計定義が含まれています。 アプリケーションのカスタマイズ内容は、拡張モデルで定義されます。

1. **アプリケーション カスタマイズの新しいモデルを作成します。** 拡張モデルに関する詳細については、 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) を参照してください。 この例では、**アプリケーション スイート拡張子** というモデルを追加し、それはアプリケーション スイート、アプリケーション プラットフォーム、およびアプリケーション基盤パッケージを参照します。
2. **Microsoft Visual Studio で、新しいプロジェクトを作成します。** プロジェクトが拡張モデルに関連付けられていることを確認します。 次の図はプロジェクト設定を示します。

    [![Visual Studio でプロジェクト設定。](./media/app-extension-vs-project-settings.png)](./media/app-extension-vs-project-settings.png)

3. **ビジネス ドキュメントのカスタム レポートのデザインを作成します。** カスタム ソリューションが正しいレポート データ コントラクトを消費することを確認する必要があります。 アプリケーション エクスプ ローラーで、既存のアプリケーション スイート レポートを検索します。 このレポートの名前は **SalesConfirm** です。 右クリックし、**プロジェクトで複製** をクリックしてカスタム ソリューションを作成します。
4. **レポートの名前を変更して、わかりやすい名前にします。** この例では、カスタム レポートの **SalesConfirmExt** を名前付けし、標準のソリューションと区別します。 プロジェクトをコンパイルしてレポートを展開し、変更にエラーがないことを確認します。
5. **自由形式デザイナーを使用して、レポートのデザインをカスタマイズします。** **レポート** という名前のレポート デザインを選択し、右クリックして、精度デザイナーを開きます。 組織の業務要件を満たすように設計をカスタマイズします。 次の図は、**Sales confirmation** レポートのカスタム設計定義を示しています。

    [![販売確認レポートのカスタム デザイン定義。](./media/app-extension-report-designer-1024x613.png)](./media/app-extension-report-designer.png)

6. **標準のレポート コントローラーを拡張する新しい X++ クラスを追加します。** クラスに、それが既存のアプリケーション レポートのハンドラーであることを適切に表す名前を付けます。 この例では、クラスの **SalesConfirmControllerExt** の名前を変更し、他のレポート コントローラーと区別します。
7. **拡張クラスを使用して、カスタム デザインを読み込みます。** カスタム レポート デザインを参照する **メイン** メソッドを追加します。 (標準的なソリューションから **主要な** メソッドをコピーし、新しい **コントローラー** クラスへの参照を追加することができます。) 次に、標準的なソリューションを拡張するコードを示します。

    ```xpp
    class SalesConfirmControllerExt extends SalesConfirmController
    {
        public static SalesConfirmControllerExt construct()
        {
            return new SalesConfirmControllerExt();
        }
        public static void main(Args _args)
        {
            SrsReportRunController formLetterController = SalesConfirmControllerExt::construct();
            SalesConfirmControllerExt controller = formLetterController;controller.initArgs(_args, ssrsReportStr(SalesConfirmExt, Report));
            if (classIdGet(_args.caller()) == classNum(SalesConfirmJournalPrint))
            {
                formLetterController.renderingCompleted += eventhandler(SalesConfirmJournalPrint::renderingCompleted);
            }
            formLetterController.startOperation();
        }
    }
    ```

8. **新しいレポート ハンドラー (X++) クラスをプロジェクトに追加します。** クラスに、それが印刷管理に基づくドキュメントのハンドラーであることを適切に表す名前を付けます。 この例では、クラスの **PrintMgtDocTypeHandlerExt** の名前を変更し、他のオブジェクト ハンドラーと区別します。
9. **デリゲート ハンドラー メソッドを追加して、カスタム レポートの使用を開始します。** この例では、次のコードを使用して **PrintMgtDocTypeHandlerExt** クラスの **getDefaultReportFormatDelegate** メソッドを展開します。

    ```xpp
    class PrintMgtDocTypeHandlersExt
    {
        [SubscribesTo(classstr(PrintMgmtDocType), delegatestr(PrintMgmtDocType, getDefaultReportFormatDelegate))]
        public static void getDefaultReportFormatDelegate(PrintMgmtDocumentType _docType, EventHandlerResult _result)
        {
            switch (_docType)
            {
                case PrintMgmtDocumentType::SalesOrderConfirmation:
                     _result.result(ssrsReportStr(SalesConfirmExt, Report));
                     break;
            }
        }
    }
    ```

10. **アプリケーションのレポートのメニュー項目を拡張します。** アプリケーション エクスプ ローラーで、既存のアプリケーション スイート メニュー項目を検索します。 このメニュー項目の名前は **SalesConfirmation** です。 右クリックし、**拡張子の作成** をクリックします。 デザイナーで新しい拡張オブジェクトを開いて、**オブジェクト** プロパティの値を **SalesConfirmControllerExt** に設定し、ユーザー ナビゲーションを拡張されたソリューションにリダイレクトします。
11. **カスタム ビジネス ドキュメントを使用するため、印刷管理設定を更新してください。** この例では、**売掛金勘定** &gt; **セッテイ** &gt; **フォーム** &gt; **フォーム設定** の順に移動します。 **印刷管理** をクリックし、ドキュメントの構成設定を検索し、カスタム デザインを選択します。 次の図は、変更がコンパイルされた後の印刷管理設定を示しています。

    [![コンパイル後の印刷管理設定。](./media/app-extension-print-mgt-after-1024x608.png)](./media/app-extension-print-mgt-after.png)

これで、ビジネス ドキュメントのカスタマイズが完了しました。 アプリケーションでトランザクションを処理するとき、ビジネス ドキュメントのカスタム レポート デザインがユーザーに提示されるようになります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
