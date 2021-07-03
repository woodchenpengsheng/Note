# 最终目标
## win
1. ctrl + right光标跳跃到下一个单词
2. ctrl + left光标跳跃到前一个单词
3. end光标跳跃到行末
4. home光标跳跃到行首
## mac
1. alt + right光标跳跃到下一个单词
2. alt + left光标跳跃到前一个单词
3. Fn + left光标跳跃到行首
4. Fn + right光标跳跃到行末

# 实现方案
## 1. 快捷键响应逻辑
- 实现一个类继承自Extension,绑定keys回调
- 移除原来的rewriteKeymap中关于mod + Arrow等的处理
## 2. 如何进行跳转
## 3. 设置光标的逻辑
## 4. Black Swan
# 现有的光标跳转的相关逻辑
- `jumpToHomeOrEnd`
- `getSideCoordsAtPos`