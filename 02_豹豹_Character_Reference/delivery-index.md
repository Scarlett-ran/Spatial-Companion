# Spatial Companion「豹豹」交付索引

## 最终图片

1. 主角色三分之四视角：`main-character-reference.png`
2. 正面全身：`01-front-fullbody.png`
3. 左侧面全身：`02-side-fullbody.png`
4. 背面全身：`03-back-fullbody.png`
5. 蜷缩睡觉：`04-curled-sleep.png`
6. 从睡眠中醒来并抬头：`05-waking-head-up.png`
7. 靠近并嗅闻用户的手：`06-sniffing-hand.png`
8. 用头部蹭用户的手：`07-nuzzling-hand.png`
9. 互动结束后安静趴下：`08-settled-rest.png`
10. 睡眠表情：`09a-expression-sleeping.png`
11. 好奇表情：`09b-expression-curious.png`
12. 放松表情：`09c-expression-relaxed.png`
13. 睡觉姿势透明素材：`10-sleep-transparent.png`
14. 中性坐姿透明素材：`11-neutral-transparent.png`
15. 参考集总览：`reference-set-overview.png`（仅用于快速检查；上面 14 张文件仍是独立交付物）

## 设计与提示词

- 最终角色设计说明：`character-design.md`
- 主角色生成提示词：`main-character-prompt.md`
- 所有派生图片提示词及统一限制项：`derivative-prompts.md`

## 统一角色限制

保持同一只原创三维幼年海豹：温暖象牙白短密天鹅绒绒毛；额头无月牙、无符号、无装饰图案；深午夜蓝圆杏形眼睛；小三角鼻；灰炭色圆润心形口鼻区；圆头、短颈、低矮水滴形身体；两只扁平桨状前鳍、两只圆润后鳍和后鳍之间一个极短尾突；无外耳廓；鳍端柔和石墨灰。不得改变头身比例、眼距、口鼻大小、毛发长度、材质、毛色分布和渲染风格。

避免新的斑点或花纹、兔耳或猫耳、兽爪或腿、长尾、翅膀、角、多余肢体或尾巴、衣服、项圈、配饰、夸张动漫眼、塑料材质、湿黏毛发、文字、标志、水印、风景、漂浮特效、光环、强烈阴影、裁切、遮挡和解剖错误。除 `06` 与 `07` 外不得出现人物或手。

## AI 视频角色参考建议

- **核心身份参考**：`main-character-reference.png`、`01-front-fullbody.png`、`02-side-fullbody.png`、`03-back-fullbody.png`。适合作为角色一致性、建模和多视角身份输入。
- **表情一致性参考**：`09a-expression-sleeping.png`、`09b-expression-curious.png`、`09c-expression-relaxed.png`。适合约束眼睑、目光、口鼻和情绪强度。
- **动作与镜头节拍参考**：`04-curled-sleep.png`、`05-waking-head-up.png`、`06-sniffing-hand.png`、`07-nuzzling-hand.png`、`08-settled-rest.png`。可按“睡眠—醒来—接近—触碰—安静结束”的 20 秒叙事顺序使用。

## 第三人称镜头合成建议

- `06-sniffing-hand.png` 与 `07-nuzzling-hand.png`：已有手部关系、接触方向与视线，适合直接作为第三人称互动镜头构图参考。
- `10-sleep-transparent.png`：适合将睡眠角色合成到桌面、地板、沙发、床边或 XR 空间锚点。
- `11-neutral-transparent.png`：适合通用第三人称镜头、静止建立镜头和后续空间定位合成。
- `04-curled-sleep.png`、`05-waking-head-up.png`、`08-settled-rest.png`：适合作为合成前的姿态、姿势和接地关系参考。

## 验证结果

- 14 张最终角色图片均为独立文件且内容哈希不同。
- 两张透明素材均为 RGBA PNG，并具有真实透明像素。
- 最终总览视觉 QA 通过：未发现月牙符号、错误肢体、明显身份漂移、透明底 matte、残留地面阴影、光晕、散点或裁切。
