##初始專案
	git clone 網址.git						拉取專案
	git add . 								加入索引(確定索引OK，在執行 更新紀錄)
	git status								檢查狀態(檢查新增的檔案)
	git commit -m "update: 更新紀錄名稱"	提交更新(更新紀錄)
	git push origin 分支					推送


##團隊-個人拉取專案
	git checkout -b feature/功能名稱		創建分支
	git fetch origin main					更新遠端分支追蹤
	git rebase origin/main					將遠端分支狀態整合至本地目前分支
	git add .								加入索引(確定索引OK，在執行 更新紀錄)
	git commit -m "pdate: 更新紀錄名稱"		提交更新(更新紀錄)
	git push origin feature/功能名稱		推送
	至 git提交 PR


##PR審核
	git checkout 要檢查的分支代號
	git chenkput 檢查完後回到原本分支
	通過 or 不通過 PR
	若通過則需要遠端拉取倉庫同步至本地
	git fetch origin main					更新遠端分支追蹤
	git merge origin/main					本地更新同步至遠端狀態


##解決衝突
	git checkout 要檢查的分支代號
	git rebase origin/main					將遠端分支狀態整合至本地目前分支
	git add .
	git rebase --contiune					解決了合併衝突並送出
	git branch 要檢查的分支代號				切換分支
	git checkout 要檢查的分支代號
	git push 要檢查的分支代號
	git fetch origin main					更新遠端分支追蹤
	git rebase origin/main					將遠端分支狀態整合至本地目前分支
