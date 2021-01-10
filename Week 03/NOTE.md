学习笔记
LL算法构建AST - 字符串处理
AST - 抽象语法树
通过编程语言分词>分词后构成层层嵌套的语法树树形结构>解析代码>执行
LL = Left (从左到右扫描) Left (从左到右规约)

四则运算包括
TokenNumber: 数字
Operator: 运算符
Whitespace: 空格
LineTerminator: 换行符

乘法表达式
<MultiplicativeExpression>::=
<Number>
|<MultiplicativeExpression><*> <Number>
|<MultiplicativeExpression> </> <Number>

加法表达式
<AdditiveExpression>::=
<MultiplicativeExpression>
|<AdditiveExpression><+><MultiplicativeExpression>
|<AdditiveExpression><-><MultiplicativeExpression>

整体表达式
<Expression>::=
<AdditiveExpression><EOF>
