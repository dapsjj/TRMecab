import MeCab
import csv

mecab = MeCab.Tagger("-Ochasen") #有词性标注的兼容格式
title = [['キーワード','字典形','品詞']]
cmp_nouns = mecab.parse('私たちは、新しい流通のステージに向けて、1日1日少しずつ、地道に確実に、当たり前のことを当たり前に行ってまいります。かけがえのない生涯を、夢ある人生をかけるにふさわしいロマンに向かって、トライする仲間がいる会社が、私たちトライアルカンパニーです。')
every_row = cmp_nouns.split('\n')
save_word_list = []
for every_attribute_line in every_row:
    every_attribute_array = every_attribute_line.split('\t')
    if len(every_attribute_array) > 3:
        save_word_list.append([every_attribute_array[0].strip(),every_attribute_array[2].strip(),every_attribute_array[3].strip()])

with open(r'D:/20181031mecabResult.csv', 'w', newline='', encoding='utf-8') as f:
    writer = csv.writer(f)
    writer.writerows(title)
    writer.writerows(save_word_list)
