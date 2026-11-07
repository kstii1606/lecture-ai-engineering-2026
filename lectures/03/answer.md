# 第3回 解答

## 演習

- 第1回（素のLLM）とエージェントの回答の違い：
- `--trace` で見えたツール呼び出し（ツール名と引数）：
- 1つの質問での LLM 呼び出し回数（`requests`）：
- 追加したツールと、docstring に書いた説明：

## 宿題

- 取り組んだレベル：基礎
- やったこと：
    app/tools.py の docstring を書き換え
- 結果：
    1回目
    [model] gemini-3.5-flash-lite
    第2回の内容から確認問題を1問出題します！

    **【問題】**
    「エポック」の意味を説明してください。

    （第2回）

    [tool call]   make_quiz({'lecture': 2})
    [tool return] make_quiz -> {"lecture": 2, "question": "「エポック」の意味は？", "answer": "学習データ全体を1周学習することを1エポックと数える。回数を増やしすぎると過学習しやすい。"}…
    [usage] RunUsage(cost=Decimal('0.0003851'), details={'text_prompt_tokens': 867}, input_text_tokens=867, input_tokens=867, output_tokens=50, requests=2, tool_calls=1)

    2回目
    [model] gemini-3.5-flash-lite
    第2回から、復習用の確認問題を2問出しますね！

    **第1問**
    「量子化」の意味は？

    **第2問**
    「過学習」の意味は？

    それぞれの答えを考えてみてくださいね。詳しい解説やヒントが欲しいときはいつでも聞いてください！

    第2回

    [tool call]   make_quiz({'lecture': 2})
    [tool return] make_quiz -> {"lecture": 2, "question": "「量子化」の意味は？", "answer": "モデルの重みを少ないビット数（例：16ビットから4ビット）で表し、メモリ使用量や計算量を減らす技術。精度は少し下がることがある。"}…
    [tool call]   make_quiz({'lecture': 2})
    [tool return] make_quiz -> {"lecture": 2, "question": "「過学習」の意味は？", "answer": "学習データにだけ過度に適合し、未知の入力に対する性能が落ちる状態。学習に使わない検証データで性能を測って気づく。"}…
    [usage] RunUsage(cost=Decimal('0.0006763'), details={'text_prompt_tokens': 1446}, input_text_tokens=1446, input_tokens=1446, output_tokens=97, requests=3, tool_calls=2)

- 気づき・疑問：
    docstringの書き換えが小さかったのか、上記の例では日本語の表現が変わったように見えるレベルであった
    エージェントがユーザーへ返す「出力の質・内容・安定性」に違いが見られた
