---
title: MS 登録が共同作業します。
description: Azure Active Directory 組織を設定するまたは MS の共同作業が、個人 Microsoft アカウント (MSA) を必要とするデベロッパー センター ダッシュ ボードを使用します。
author: ikhapova
ms.author: ikhapova
ms.date: 12/12/2017
keywords: パートナーのアクセス、アクセス許可、登録、登録、オンボード、パートナーからのフィードバック、ビルドのダウンロード、ダウンロードの仕様、バグ、Microsoft Connect、SysDev バグ、デベロッパー センターのバグ
ms.openlocfilehash: b58468950a70c17ebb3959d4b3bbd30b4cf862a0
ms.sourcegitcommit: 8ae2ead732e03d8a9865797bb9f40818780036e9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2018
ms.locfileid: "43055110"
---
# <a name="register-with-microsoft-collaborate"></a>マイクロソフトの登録が共同作業します。

Microsoft の共同作業、プログラムでは、登録が必要です。 デベロッパー センター アカウントがある場合は、ログインし、共同作業との対話に使用できます。 コンテンツをダウンロードしたり、フィードバックを送信することが、前に、engagement に参加する必要があります。 いくつかの取り組みに Microsoft からの招待が必要と**Engagement 所有者**または**Power User** (ときに、組織にすでに追加されて、engagement)。 その他の契約が**オープン**の参加をユーザーにします。

## <a name="the-account-signup-process"></a>アカウントのサインアップ

1.  移動し、 [ https://aka.ms/collaborate ](https://aka.ms/collaborate)ページ。 
2.  Microsoft アカウントを使用して署名されていない場合は、今すぐサインインまたは新しい Microsoft アカウントを作成します。 ここで使用する Microsoft アカウントを Microsoft の共同作業へのサインインに使用するとなります。
3.  Microsoft の共同作業する登録されていない場合、システムは自動的にリダイレクトする、[登録ページ](https://go.microsoft.com/fwlink/?linkid=851519)します。
4.  Live する、または、ビジネスが配置されている国/地域を選択します。 これを後で変更することはできません。
5.  アカウントの種類を選択します (個人または会社)。 この後で変更するには、これを必ず適切な種類のアカウントを選択することはできません。
6.  入力、**発行者表示名**(50 文字以下) を使用することです。 共同作業とやり取りする場合、この名前は使用するように、慎重に選択 (コンテンツをダウンロードするなど、フィードバックの送信) します。 会社アカウントでは、必ず、組織の名前または登録されているビジネス名を使用します。 他のユーザーが既に選択されている名前を入力するか、場合に、その名前を使用する権利を持っている人が表示されたら、私たちは許可されませんの名前を使用することに注意してください。 

  > [!NOTE]
  > ここで入力した名前を使用する権限があることを確認します。 商標および他のユーザーが持っているか、選択した名前の著作権、自分のアカウントが閉じられます可能性があります。 他のユーザーを商標や他の法的な権利を持つ発行者表示名を使用している場合[Microsoft にお問い合わせください](http://go.microsoft.com/fwlink/p/?LinkId=233777)します。    

7.  アカウントを使用する連絡先情報を入力します。

  > [!NOTE]
  > この情報は、アカウント関連の事柄についての連絡に使用します。 たとえば、登録を完了した後電子メールの確認メッセージを受信します。

   企業として登録する場合、名前、電子メール アドレス、および会社のアカウントを承認するユーザーの電話番号を入力する必要もあります。

8.  アカウント情報を確認し、すべて正しいことを確認します。 次に、読み取りし、の条項に同意、[共同作業を行う契約](https://go.microsoft.com/fwlink/?linkid=849107)します。 読み、条項を承諾して、示すために、ボックスを確認します。

9.  クリックして**完了**をお客様の登録を確認します。  

## <a name="additional-guidelines-for-company-accounts"></a>会社のアカウントの追加のガイドライン

会社のアカウントを作成するときをお勧めこれらのガイドラインに従うことは、複数のユーザーがアカウントにアクセスする必要がある場合に特にです。

> [!IMPORTANT]
> デベロッパー センター アカウントにアクセスする複数のユーザーを許可するのには、個々 のユーザーにロールを割り当てる Azure Active Directory を使用してお勧めします。 各ユーザー各自のサインインして、デベロッパー センター アカウントにアクセスできる、Azure AD の資格情報。 詳細については、次を参照してください。[アカウント ユーザーを管理する](/windows/uwp/publish/manage-account-users.md)します。

-   既にに属していないか、別のユーザーなどの電子メール アドレスを使用して Microsoft アカウントを作成MyCompany_DevCenter@outlook.comです。 いないことができます、会社のドメインで電子メール アドレスを使用する会社が既に Azure AD を使用している場合に特にです。
-   後でアプリの開発用の Windows プログラムに参加し、デベロッパー センター アカウントを再利用する場合は、お勧め Windows プログラムを最初に登録し、Microsoft の共同作業に参加すること。 それ以外の場合は、これらのプログラムの個別のアカウントを作成する必要があります。
-   拡張機能が必要としないと、主要なチーム メンバーにアクセスする会社の電話番号を追加します。

## <a name="how-to-associate-your-dev-center-account-with-azure-active-directory-and-manage-users"></a>デベロッパー センターを関連付ける方法と Azure Active Directory アカウントし、ユーザーの管理

Azure Active Directory を使用して、追加して、デベロッパー センター アカウントに追加のユーザーを管理することができます。 ロールまたは各ユーザーにカスタムのアクセス許可を定義できます。 

最初とユーザーを追加および管理できる Azure Active Directory の組織のデベロッパー センター アカウントを関連付ける必要があります。 

このセクションには、次の方法について説明します。

-   [デベロッパー センター アカウントを Azure Active Directory に関連付ける](/windows/uwp/publish/associate-azure-ad-with-dev-center)
-   [ユーザー、グループ、およびデベロッパー センター アカウントに Azure AD アプリケーションを追加します。](/windows/uwp/publish/add-users-groups-and-azure-ad-applications)
-   [ロールとアカウントのユーザーのカスタム アクセス許可を設定します。](/windows/uwp/publish/set-custom-permissions-for-account-users)

> [!TIP]
> デベロッパー センターは、マルチ ユーザー管理とロール割り当てのための Azure Active Directory を活用します。 組織が既に Office 365 または Microsoft の他のビジネス サービスを使用する場合、AAD が既にあります。 それ以外の場合、追加料金なしでデベロッパー センター内から新しい AAD テナントを作成することができます。

## <a name="how-to-log-in-to-the-ms-collaborate-portal"></a>MS の共同作業ポータルにログインする方法

1. MS に移動します。 共同作業: [ https://aka.ms/collaborate](https://aka.ms/collaborate)します。

2.  資格情報をログなります。 これは、デベロッパー センター アカウントの資格情報です。 1 つ以上のアカウントを使っている場合は、デベロッパー センターにサインアップするために使用する適切なアカウントを選択します。 Microsoft エイリアス アカウント (MSA) または Active Directory の組織アカウントを指定できます。 ログインする前にしていない場合は、パスワードを入力する必要があります。

3. Microsoft の共同作業のダッシュ ボードが表示され、契約、パッケージ、およびフィードバックを表示するには、ログインした後を参照してくださいに構成されます。 プログラムまたは契約のメンバーでない場合は、一覧は空白になります。 コンテンツやフィードバックと対話する契約に追加する必要があります。 

