---
title: U クラス
description: 文字 U で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 51691
ms.assetid: 92bfbb9c-4f45-464a-8ccb-71fb227780fe
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d2d1f5bdf10c538b3d398bc2ac22d23498da1f5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183359"
---
# <a name="u-classes"></a>U クラス

[!include [banner](../includes/banner.md)]

文字 U で始まるシステム API クラス。

<a name="class-unitofwork"></a>クラス UnitofWork
----------------

    class UnitofWork extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                       | 説明                                         |
|--------------------------------------------------------------|-----------------------------------------------------|
| public boolean getByKey(Common record)                       |                                                     |
| public void updateonSaveChanges(Common record)               |                                                     |
| public void saveChanges(\[UserConnection user\_connection\]) |                                                     |
| public void deleteonSaveChanges(Common record)               |                                                     |
| public void insertonSaveChanges(Common record)               |                                                     |
| public void finalize()                                       |                                                     |
| public void new()                                            | UnitofWork クラスの新しいインスタンスを初期化します。 |
| public void clear()                                          |                                                     |

### <a name="method-getbykey"></a>メソッド getByKey

    public boolean getByKey(Common record)

#### <a name="parameters"></a>パラメーター

記録  

#### <a name="return-value"></a>戻り値

### <a name="method-updateonsavechanges"></a>メソッド updateonSaveChanges

    public void updateonSaveChanges(Common record)

#### <a name="parameters"></a>パラメーター

記録  

### <a name="method-savechanges"></a>メソッド saveChanges

    public void saveChanges([UserConnection user_connection])

#### <a name="parameters"></a>パラメーター

user\_connection  

### <a name="method-deleteonsavechanges"></a>メソッド deleteonSaveChanges

    public void deleteonSaveChanges(Common record)

#### <a name="parameters"></a>パラメーター

記録  

### <a name="method-insertonsavechanges"></a>メソッド insertonSaveChanges

    public void insertonSaveChanges(Common record)

#### <a name="parameters"></a>パラメーター

記録  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

UnitofWork クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-clear"></a>メソッド clear

    public void clear()

## <a name="class-userconnection"></a>クラス UserConnection
    class UserConnection extends Connection

UserConnection クラスは、主要な接続と同じログオン プロパティに基づいて、SQL データベースへの補助接続を表します。

### <a name="remarks"></a>備考

SQL ステートメントが実行され、結果が UserConnection クラスのコンテキストで返されます。 UserConnection クラスを使用して、別個のトランザクション スコープを取得できます。

注記: ユーザー接続リークを防ぐため、finally ブロックで Userconnection.finalize() を呼び出す必要があります。  オープン ユーザー接続の数がサーバー上で制限されており、制限に達すると、それ以上接続を開くことができなくなり、ビジネス ロジックのエラーになる可能性があります

### <a name="examples"></a>例

    static void example()  
    { 
        UserConnection Con;
        try
        {
            Statement Stmt; 
            Str sql; 
            ResultSet R; 
            SqlStatementExecutePermission perm; 
            Con = new UserConnection(); 
            sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
            Stmt = Con.createStatement(); 
            perm = new SqlStatementExecutePermission(sql); 
            // Check for permission to use the statement. 
            perm.assert(); 
            R = Stmt.executeQuery(sql); 
            while ( R.next() ) 
            { 
                print R.getString(1); 
            } 
        }
        finally
        {
            con.finalize();
        }
     }

### <a name="methods"></a>方法

| 方法                                                | 説明                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| public void new(\[boolean generateNewTransactionID\]) | Connection クラスの新しいインスタンスを初期化します。 |

### <a name="method-new"></a>メソッド new

Connection クラスの新しいインスタンスを初期化します。

    public void new([boolean generateNewTransactionID])

#### <a name="parameters"></a>パラメーター

generateNewTransactionID  

## <a name="class-usermenulist"></a>クラス UserMenuList
    class UserMenuList extends TreeNode

UserMenuList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                               | 説明 |
|--------------------------------------|-------------|
| public void createMenu(\[str name\]) |             |

### <a name="method-createmenu"></a>メソッド createMenu

    public void createMenu([str name])

#### <a name="parameters"></a>パラメーター

名前  

## <a name="class-usersetup"></a>クラス UserSetup
    class UserSetup extends TreeNode

UserSetup クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。

### <a name="remarks"></a>備考

このクラスは、主に SysUserSetup フォームで使用されます。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                  | 説明 |
|-----------------------------------------|-------------|
| public boolean xRef(\[boolean enable\]) |             |
| public void setUserSetup(Common cursor) |             |
| public void setDefaults(Common cursor)  |             |

### <a name="method-xref"></a>メソッド xRef

    public boolean xRef([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

#### <a name="return-value"></a>戻り値

### <a name="method-setusersetup"></a>メソッド setUserSetup

    public void setUserSetup(Common cursor)

#### <a name="parameters"></a>パラメーター

cursor  

### <a name="method-setdefaults"></a>メソッド setDefaults

    public void setDefaults(Common cursor)

#### <a name="parameters"></a>パラメーター

cursor  

## <a name="class-utilfile"></a>クラス UtilFile
    class UtilFile extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                      |
|-------------------------------------------------------------|------------------------------------------------------------------|
| public boolean aodFileExist(UtilEntryLevel layer)           |                                                                  |
| public int importAODFile(UtilEntryLevel layer, int modelId) |                                                                  |
| public str layers()                                         |                                                                  |
| public boolean needReindex()                                |                                                                  |
| public void check(str layer, str action)                    |                                                                  |
| public void new(str fileType)                               | Object クラスの新しいインスタンスを初期化します。                  |
| public void reindex()                                       | X++ コードとメタデータの作成、読み取り、更新、および削除ができます。 |
| public void flushCache()                                    |                                                                  |

### <a name="method-aodfileexist"></a>メソッド aodFileExist

    public boolean aodFileExist(UtilEntryLevel layer)

#### <a name="parameters"></a>パラメーター

 レイヤー  

#### <a name="return-value"></a>戻り値

### <a name="method-importaodfile"></a>メソッド importAODFile

    public int importAODFile(UtilEntryLevel layer, int modelId)

#### <a name="parameters"></a>パラメーター

 レイヤー  

<!-- -->

modelId  

#### <a name="return-value"></a>戻り値

### <a name="method-layers"></a>メソッド layers

    public str layers()

#### <a name="return-value"></a>戻り値

### <a name="method-needreindex"></a>メソッド needReindex

    public boolean needReindex()

#### <a name="return-value"></a>戻り値

### <a name="method-check"></a>メソッド check

    public void check(str layer, str action)

#### <a name="parameters"></a>パラメーター

 レイヤー  

<!-- -->

アクション  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(str fileType)

#### <a name="parameters"></a>パラメーター

fileType  

### <a name="method-reindex"></a>メソッド reindex

X++ コードとメタデータの作成、読み取り、更新、および削除ができます。

    public void reindex()

#### <a name="remarks"></a>備考

この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

#### <a name="examples"></a>例

次の例では、UtilFile.reindex メソッドを呼び出します。 変更を実行する前に、ユーザーが必要なセキュリティ キーを持っているかどうかを確認します。

    server static public void Main(Args _args) 
    { 
        UtilFile u; 
        u = new UtilFile("util"); 
        if (u) 
        { 
            u.reindex(); 
        } 
    }

### <a name="method-flushcache"></a>メソッド flushCache

    public void flushCache()



