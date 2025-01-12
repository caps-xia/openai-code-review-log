根据提供的`git diff`记录，以下是针对`.github/workflows/main-maven-jar.yml`和`.github/workflows/main-remote-jar.yml`两个工作流程文件的代码评审：

### `.github/workflows/main-maven-jar.yml` 评审

#### 变更点：
- 修改了触发工作流程的分支，从`master`更改为`master-close`。

#### 评审意见：
1. **目的**：不清楚分支`master-close`的具体含义。如果`master-close`是一个特定的分支，那么这个更改可能是为了区分某些特定的代码库状态或者分支。
2. **一致性**：如果`master-close`是一个标准分支，则应确保所有工作流程文件中相关的触发条件保持一致。
3. **文档**：建议在工作流程的文档中说明`master-close`分支的作用，以便团队成员理解这些更改背后的原因。

### `.github/workflows/main-remote-jar.yml` 评审

#### 变更点：
- 修改了触发工作流程的分支，从`master-close`更改为`master`。

#### 评审意见：
1. **目的**：同样地，不清楚分支`master-close`和`master`之间的关系。如果`master-close`是一个特定分支，那么这个更改可能是为了与`main-maven-jar.yml`中的更改保持一致。
2. **一致性**：如果`master`是主分支，则确保所有相关的工作流程文件都使用`master`作为触发分支。
3. **文档**：应确保工作流程文档更新，以反映任何分支名称变更的原因和目的。

### 总结
- 确保所有工作流程文件的触发条件保持一致，避免混淆。
- 如果分支名称有特殊含义，确保在文档中明确说明。
- 保持工作流程文件的清晰和一致性，以便于维护和理解。