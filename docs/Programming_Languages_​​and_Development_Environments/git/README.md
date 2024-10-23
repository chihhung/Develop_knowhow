[< backto專體開發從業人員參考](../../../README.md)

我的notebook, notebook是windows 10,同時使用github,github有二個帳號,一個私人一個公司, 公司的gitlab有一帳號, 如何在notebook上設立git 同時可處理多個帳號

在 Windows 10 的 notebook 上配置 Git，以便同時處理多個 GitHub 和 GitLab 帳號，你可以透過 SSH 和 Git 的配置來完成，步驟如下：

1.生成 SSH 金鑰並配置多個帳號
為每個帳號生成獨立的 SSH 金鑰（如果尚未生成）：

bash
```
ssh-keygen -t rsa -C "<your_personal_email@example.com>" -f ~/.ssh/id_rsa_personal
```
```
ssh-keygen -t rsa -C "<your_company_email@example.com>" -f ~/.ssh/id_rsa_company
```
然後將生成的 id_rsa_personal.pub 和 id_rsa_company.pub 添加到對應 GitHub 和 GitLab 帳號的 SSH Keys 設定中。

2.配置 SSH Config 檔案
編輯或創建 ~/.ssh/config 檔案，指定每個 SSH 金鑰的使用規則：

bash

# GitHub 個人帳號
```
Host github.com-personal
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_personal
```
# GitHub 公司帳號
```
Host github.com-company
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_company
```
# GitLab 公司帳號
```
Host gitlab.com-company
  HostName gitlab.com
  User git
  IdentityFile ~/.ssh/id_rsa_company
```
3.克隆和操作倉庫
使用自定義的 SSH 配置來克隆倉庫。例如：

克隆個人 GitHub 倉庫：

bash
```
git clone <git@github.com-personal>:yourusername/yourrepository.git
```
克隆公司 GitHub 倉庫：

bash
```
git clone <git@github.com-company>:yourcompany/yourrepository.git
```
克隆公司 GitLab 倉庫：
bash
```
git clone <git@gitlab.com-company>:yourcompany/yourrepository.git
```
4.配置 Git 使用者資訊

如果需要在不同的倉庫中使用不同的使用者資訊，可以在每個倉庫中單獨設定：
bash
```
cd /path/to/your/repository
git config user.name "Your Name"
git config user.email "<your_email@example.com>"
```
或者在全域配置中設置默認的使用者資訊：
bash
```
git config --global user.name "Your Default Name"
git config --global user.email "<your_default_email@example.com>"
```
5. 驗證 SSH 配置
測試 SSH 配置是否正確：

bash
```
ssh -T <git@github.com-personal>
ssh -T <git@github.com-company>
ssh -T <git@gitlab.com-company>
```