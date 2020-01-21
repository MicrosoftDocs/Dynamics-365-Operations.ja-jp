---
title: ワークフローへの休暇要求の送信
description: この記事では、MyLeaveRequests submit () アプリケーション プログラミング インターフェイス (API) に関する参照資料を提供します。
author: gboyko
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: gboyko
ms.search.validFrom: 2019-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97a755dd655ac84b99ccf9f95c4acfc465f323d3
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898932"
---
# <a name="submit-a-leave-request-to-workflow"></a>ワークフローへの休暇要求の送信

## <a name="overview"></a>概要

Microsoft Dynamics 365 Talent では、MyLeaveRequests submit () アプリケーション プログラミング インターフェイス (API) を使用して、休暇要求をワークフローに送信できます。 この API は、MyLeaveRequests OData エンティティでアクションとして公開されます。

## <a name="prerequisites"></a>必要条件

休暇要求はデータベースに保存する必要があり、MyLeaveRequests エンティティを通じて取得できる必要があります。

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[Talent データ API による認証](api-odata-authentication.md) を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

## <a name="https-request"></a>HTTPS 要求

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

この要求は OData の標準に準拠しています。 {requestId}、{leaveType}、{leaveDate}、{dataArea} の各パラメーターは、MyLeaveRequests エンティティの複合ナチュラル キーを構成するフィールドを参照します。

> [!NOTE]
> MyLeaveRequests エンティティのフィールドは休暇要求の個々の行を参照しますが、送信 API を呼び出すと、休暇要求全体 (すべての行) がワークフローに送信されます。

### <a name="request-headers"></a>要求ヘッダー

| 表題         | 金額                     |
|----------------|---------------------------|
| 承認  | ベアラー {token} (必須) |
| Content-Type   | アプリケーション /json          |

### <a name="request-body"></a>要求の本文

このメソッドの要求の本文を供給しないでください。

### <a name="response"></a>応答

成功したときの応答は常に **204 No Content (内容なし)** です。

未承認の呼び出し元は、**401 Unauthorized (未承認)** または **403 Forbidden (許可されていません)** といった応答を受け取ります。

送信が失敗した場合 (たとえば検証のため)、応答は **500 Server Error (サーバー エラー)** になり、応答本文には詳細を含む JSON オブジェクトが含まれます。

## <a name="example"></a>例

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>検証とエラー メッセージ

送信 API の呼び出しの一環として、Talent は送信前にビジネス ロジック検証を実行します。これにより、休暇要求は送信に対して有効な状態にあることが保証されます。 検証が失敗した場合に応答で受け取る可能性のあるエラー メッセージは次のとおりです。

 - この要求による '{LeaveTypeId}' の残日数は、{date} の最小許容残日数を下回っています。
 - 完了状態の休暇申請要求は送信できません。
 - 変更が行われていないため、要求を送信または保存できません。 量または休暇タイプを追加または更新して、もう一度やり直してください。
 - 入力された休暇申請には、既存の保留中の申請と同じ休暇タイプおよび日付が 1 日以上含まれています。 変更を加えるには、既存の要求を取り消してください。
 - 理由コード '{ReasonCodeId}' は申請における休暇のタイプのいずれにも適用されません。
 - 休暇タイプ '{LeaveTypeId}' には理由コードが必要です。 適切なタイプと理由コードを選択します。
 - 休暇申請が正常に送信されていません。 休暇申請は下書きの要求として保存されました。

## <a name="see-also"></a>参照

[MyLeaveRequests](api-myleaverequests-overview.md)