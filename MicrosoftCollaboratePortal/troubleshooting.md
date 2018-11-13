---
title: トラブルシューティング ガイド
description: 一般的な問題をトラブルシューティングする方法
author: ikhapova
ms.author: ikhapova
ms.date: 08/02/2018
keywords: troubeshooting、問題、登録、アクセス、アカウント、フィードバック
ms.openlocfilehash: 460a8b3e44e294de6ce3c93b6496e5f0caf9d76e
ms.sourcegitcommit: 13d67929e8cb9c0150596f046502ea046b0c4332
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2018
ms.locfileid: "51561533"
---
# <a name="how-to-troubleshoot-common-issues"></a>一般的な問題をトラブルシューティングする方法
このページは、一般的な問題のトラブルシューティング ガイドを提供します。

## <a name="sign-in"></a>サインイン

### <a name="microsoft-account-sign-in"></a>Microsoft アカウントでサインイン
Microsoft の共同作業の web サイトにサインインできない場合は、これらの推奨事項を試してください。 
- 完全な電子メール アドレスを使用してサインインするかどうかを確認します。
- Microsoft アカウント サービスの状態を確認してください。
- パスワードを正しく入力したことを確認します。 パスワードは大文字小文字を区別します。 パスワードを忘れた場合は、Microsoft アカウントに移動[パスワードをリセット](https://account.live.com/password/reset)ページ。
- お使いのブラウザーが cookie を許可する構成されていることを確認します。 お使いのブラウザーで cookie を許可しない場合は、Microsoft アカウントでサインインすることはできません。
- ブラウザーのキャッシュ、cookie、一時ファイル、および格納されているその他の閲覧履歴を消去してください。 ブラウザーを閉じてから、新しい InPrivate ブラウズ セッションを開きます。

### <a name="browser-hangs-or-shows-page-cant-be-displayed-error-when-signing-in-to-dev-center"></a>ブラウザーがハングまたはデベロッパー センターにサインインするときに、「ページを表示できません」エラーを示しています
デベロッパー センター/共同作業するユーザー名とパスワードを入力した後に、これらの問題またはエラーのいずれかを表示します。
- お使いのブラウザーがハングまたは応答しなくなります。
- 「ページを表示できません」エラーが発生します。
- "ERR_TOO_MANY_REDIRECTS"ことを示すエラーが発生します。
- 「Hmm に到達できませんこのページです」というエラーが発生します。
- デベロッパー センターから、招待メールに同意して、このメッセージを取得します。

> ...... としてアプリケーションへのアクセスに招待されました。
> ただし、この作業を作成できませんまたは学校アカウントのため... が、オンプレミスのフェデレーション ドメインが AD。
> オンプレミスで正しく設定されていることを確認する、管理者にお問い合わせください AD この招待を承諾することができますを再試行します。

#### <a name="why-this-is-happening"></a>なぜこれが発生
会社のメール アドレスが Microsoft Connect: アカウントでの一般的な方法であった (作業と個人アカウントは、同じ名前の共有)、個人の MSA]/[Live ID にリンクされているため、これが発生している可能性があります。 この実習では、Microsoft ではサポートされなくと、さまざまな問題につながる可能性があります。 参照してください[このブログの投稿](https://cloudblogs.microsoft.com/enterprisemobility/2016/09/15/cleaning-up-the-azure-ad-and-microsoft-account-overlap/)の詳細。

#### <a name="fixesworkarounds"></a>修正および回避
回避策では、個人の MSA アカウントの名前を変更します。 参照してください[今回](https://support.microsoft.com/en-us/help/11545/microsoft-account-rename-your-personal-account)詳細な手順です。

## <a name="registration"></a>登録

### <a name="account-registration"></a>アカウントの登録

> グローバル管理者として自分の id を検証できませんでした。 関連付ける Azure AD テナントのグローバル管理者アカウントでサインインできることを確認します。

エラーは、ユーザーが管理者特権がない作業アカウント (AAD) を使用して署名されていることを示します。 

#### <a name="fixesworkarounds"></a>修正および回避
に従って、[指示](https://docs.microsoft.com/en-us/collaborate/registration)Microsoft アカウントを使用して登録します。

#### <a name="how-to-find-global-administrator-for-your-organization"></a>組織のグローバル管理者を検索する方法
検索**グローバル管理者**組織がビッグと複数の国にオフィスがある場合は特に難しい作業をすることができます。 

##### <a name="using-azure-portal"></a>使用して**Azure Portal**:

>[!NOTE]
>
> 使用する組織のアカウントでサインインする必要があります**Azure Portal**します。 <br>
> 使用することはできません**Azure Portal**場合は、組織の管理者以外のユーザー アクセスを制限することにしました。

1. 移動します[Azure Portal](https://portal.azure.com)
2. 選択[Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview)最初の左側のメニュー
3. 選択**役割と Administrtors** 2 つ目の左側のメニュー
4. 検索**グローバル管理者**ロール一覧とメンバーを表示する をクリックします。

![ロールと管理者](images/aad-global-admin.png)

チェック アウトする方法について次の記事**グローバル管理者**ロール。
* [Azure id ソリューションを理解します。](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/understand-azure-identity-solutions#terms-to-know)
* [メンバーの表示と Azure Active Directory での管理者ロールの説明](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-manage-roles-portal)

##### <a name="using-powershell"></a>PowerShell を使用します。

>[!NOTE]
>
> PowerShell を使用して Azure AD に接続するには、組織のアカウントでサインインする必要があります。<br>

1.  管理者として起動の Windows Powershell コンソール
2.  Powershell 用 Azure AD モジュールをインストールしない場合は、このコマンドを実行します。 <br>

```
    Install-Module AzureAD
```
3.  メンバーを表示するためのこれらのコマンドを実行**グローバル管理者**ロール <br>

```  
    Connect-AzureAD  
    $role = Get-AzureADDirectoryRole | Where-Object {$_.displayName -eq 'Company Administrator'} 
    Get-AzureADDirectoryRoleMember -ObjectId $role.ObjectId | Where-Object {$_.ObjectType -eq 'User'} | Get-AzureADUser 
```

チェック アウトする方法について次の記事**PowerShell**と**Azure AD モジュール**します。
* [Windows PowerShell のインストール](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6)
* [Azure AD モジュールをインストールします。 ](https://docs.microsoft.com/en-us/powershell/azure/active-directory/install-adv2?view=azureadps-2.0#installing-the-azure-ad-module)

### <a name="invitations"></a>招待
デベロッパー センター アカウントに参加に招待された場合、は、共同作業ポータルにアクセスするには、招待を承諾する必要があります。 次に示すようなエラー メッセージを表示する場合は、同じ電子メール アドレスを使用して Microsoft が 2 つのアカウントがあることを意味します。 

> ...... としてアプリケーションへのアクセスに招待されました。<br> ただし、この作業を作成できませんまたは学校アカウントのため... が、オンプレミスのフェデレーション ドメインが AD。<br> オンプレミスで正しく設定されていることを確認する、管理者にお問い合わせください AD この招待を承諾することができますを再試行します。<br>

以下の情報は、自分でブロックを解除するための十分な情報を提供するためのものです。
Microsoft が電子メール ドメインが Azure AD で構成されている場合は、職場/学校の電子メール アドレスにリンクされている個人の Microsoft アカウントの使用量を制限するがようになりました。 場合とにアクセスできないポータルの共同作業し、Microsoft のサインイン名が MSA をアカウントでユーザーが自分の作業アカウントを構成します。 このシナリオでユーザーが次で、個人の Microsoft アカウントの名前を変更するが[手順](http://windows.microsoft.com/en-US/Windows/rename-personal-microsoft-account/):

1. サインイン、 [Your 情報ページ](https://account.microsoft.com/profile)の Microsoft アカウント。
2. 選択**を Microsoft にサインインする方法を管理**します。
3. 下を見て、**アカウント エイリアス**セクション。
  * 表示、個人用メール アドレスが既にある、この手順をスキップすることができます。
  * 場合、職場または学校の電子メール アドレスが表示されている 1 つだけを個人の電子メール アドレスを入力または Microsoft から新しいアカウントを取得し、**電子メールを追加する**または**電話番号を追加**します。
 4. 個人の電子メール アドレスがない場合 **(プライマリ エイリアス)** 横に表示されている、選択**プライマリ**をプライマリ エイリアスとして設定します。
 5. 選択**削除**アカウントから削除する職場の電子メール アドレスの横にあります。

今後にサインインする個人の Microsoft アカウント、個人用の電子メール アドレスを使用します。 一部のアプリと Windows デバイスをもう一度サインインする必要があります。

完了すると続行から送信される共同作業の招待を受け付けて[Microsoft への招待](mailto:invites@microsoft.com)エイリアス。  職場/学校の電子メール アドレスを使用して、新しい個人 Microsoft を作成する能力を妨げていないに関する詳細についてはこちらの[記事](https://cloudblogs.microsoft.com/enterprisemobility/2016/09/15/cleaning-up-the-azure-ad-and-microsoft-account-overlap/)します。

## <a name="access"></a>アクセス

### <a name="user-cannot-see-packages-andor-engagements-heshe-has-access-to"></a>ユーザーがパッケージを表示できませんまたは契約へのアクセスを持って
ほとんどのユーザーは、デベロッパー センター内の 1 つのアカウントを 1 つの AAD テナントに属しています。 いくつかの AAD テナントやデベロッパー センターでのアカウント内に存在する、ユーザーは、リソースへのアクセスを取得するには、特定の AAD テナントまたはアカウントを手動で選択する必要があります。

#### <a name="how-to-select-an-aad-tenant"></a>AAD テナントを選択する方法
画面の右上隅にバッジ アイコンをクリックします。 1 つ以上の AAD テナント内に存在する場合、使用可能な AAD テナントの一覧が表示されます。 

#### <a name="how-to-select-specific-account-for-an-aad-tenant"></a>AAD テナント用の特定のアカウントを選択する方法
アカウントの名前は、このアカウントの利用可能なプログラムの一覧の上の左側のナビゲーション ウィンドウに表示されます。 選択した AAD テナントの利用可能なアカウントのリストを開く現在表示されているアカウント名をクリックします。

## <a name="distribution-manager"></a>配布マネージャー
配布マネージャーを使用すると、エラー メッセージが表示される可能性があります。 この記事には、これらのエラー メッセージのトラブルシューティングに役立つ情報が含まれています。

### <a name="cannot-install-application"></a>アプリケーションをインストールすることはできません。

> 続行できません。  アプリケーションは形式が正しくありません。 <br>
> について、アプリケーション ベンダーに問い合わせてください。 <br>

このエラーが示す[Microsoft .NET Framework 4.6.1 (x86 または x64)](https://www.microsoft.com/en-us/download/details.aspx?id=49981)によって必要な配布マネージャーがコンピューターにインストールされていません。 すべての ClickOnce アプリケーションでは、実行する前に、.NET Framework の正しいバージョンがインストールされている必要があります。

インストールするリンクをクリックして[Microsoft .NET Framework 4.6.1 (x86 または x64)](https://www.microsoft.com/en-us/download/details.aspx?id=49981)します。

### <a name="cannot-launch-application"></a>アプリケーションを起動できません。 

> オブジェクトのインスタンスへのオブジェクト参照は設定されていません。 <br>

アプリケーションの以前のバージョンからアップグレードした場合は、このエラーを発生する可能性があります。

#### <a name="fixesworkarounds"></a>修正および回避
回避策は、削除-アプリケーション データを 1 回です。


次の手順では、正確なパスを決定できます。
1. キーを押して**Ctrl + Alt + Del**キーボードおよびタスク マネージャーを選択します。
2. 検索**Microsoft の共同作業、配布マネージャー**
3. 右クリックし、選択**ファイルの場所を開く**オプションの一覧から

![タスク マネージャー](images/TaskManager.png)

4. これなどのフォルダーに移動する必要があります。
> %Localappdata%\apps\2.0\data\xxxxxxxx.xxx\xxxxxxxx.xxx\dist.tion_xxxxxxxxxxxxxxxx_0000.0000_xxxxxxxxxxxxxxxx\Data

![配布マネージャーのフォルダー](images/DistributionManagerLocation.png)

5. 今すぐデータ パス (%localappdata%\apps\2.0\data) に移動し、同じ名前のフォルダーを検索 
> 配布します。tion_xxxxxxxxxxxxxxxx_0000.0000_xxxxxxxxxxxxxxxx\Data

![配布マネージャーのフォルダー](images/DistributionManagerDataLocation.png)

6.  フォルダーの内容を削除します。
7.  アプリケーションを再起動します。

