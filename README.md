![bash+terminal](https://i.imgur.com/jVg5NA7.jpeg)
# Config-Project-Node-Typescript
Automatically configure a Node + TypeScript + MongoDB API.

## Como funciona

Crie uma pasta com o nome do seu projeto e basta jogar com comando abaixo do curl dentro do diretória da basta que foi criada com o nome do seu projeto

## Install Script

```bash
curl -fsSL https://tinyurl.com/node22ts | bash
```

## Script

```bash
#!/bin/bash

# curl -fsSL https://tinyurl.com/node22ts | bash

set -e

echo "==========================================="
echo "  🚀 Iniciando setup Node + TypeScript...  "
echo "==========================================="

sleep 2

echo "
⣝⢮⡳⡵⣱⢱⢱⢕⢇⢧⢳⡱⡝⣜⢎⢗⢽⢕⢯⡺⣕⢯⡺⣕⢯⡺⣕⠏⠊⠉⠘⠪⢎⢗⢝⢮⢯⡺⣕⢯⡺⡜⣜⢜⠜⡌⡪⢸⠸⡸⡸⡸⡘⡜⢌⢎⢪⢸⠨⡊⡢⡳⡹⣪⡳⣝⢮⡳⡽⣕⢯⡳⡝⣎⢗⡝⡮⡓⣕⣃⣓⣕⣃⣓⣝⣪⣓⣝⠪⢯⡺⣝⢮⡳⣝⢮⢯⡺⣝⡞
⣗⡕⡯⣝⢮⣺⢸⢘⢜⢜⢆⠧⡹⡸⡸⡱⡕⣝⢵⢹⡪⡺⣜⠮⠓⠉⠀⠀⠀⠀⠀⠀⠀⠉⠳⢕⣗⢽⣪⡳⡵⡹⡸⡨⡊⢆⠪⡂⢇⢇⢇⢣⠱⡈⠢⡑⢌⠢⡑⢌⢎⢎⢗⡵⣝⢼⢕⢯⡺⣕⢗⡝⡮⡪⣇⠯⣲⡿⣟⣿⣻⣟⣿⣟⣿⣻⣟⣿⢿⣎⢞⢮⢳⢝⡮⡯⣳⢝⣞⢮
⣜⣮⡳⣕⡳⡕⡯⡺⣌⢆⢇⢇⢇⢎⠜⢜⢜⢜⢜⢼⢸⢱⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣬⡳⡱⣕⢕⠕⢌⠢⡡⢑⠌⢌⠢⡣⢪⠪⡊⠌⠢⠨⠠⡑⡨⡐⢕⢕⢕⢧⡳⣝⢭⡳⡹⣸⢪⢺⢸⢱⢕⠇⣿⣟⡷⣈⣽⡾⣗⣿⣞⣿⣺⣽⢿⣿⢸⢪⣫⡳⣝⢮⣳⡫⣞⢝
⣕⢧⡻⣜⢮⢎⢗⢝⢎⢮⡢⡣⢱⢘⢜⢐⢅⢣⠱⡱⡱⣹⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⡠⣴⣞⣷⣻⢎⢣⢣⢣⢣⢑⠅⡊⡐⠌⠄⢕⢘⠔⠕⢅⠕⠡⠡⢑⠐⡐⢌⢪⢪⢺⡸⡪⡎⡇⡇⡯⡪⡪⡊⢎⠎⡢⢑⣽⣯⡷⣿⣺⣭⣭⡷⣟⣾⣻⣾⣻⣿⢸⡱⣕⢝⢮⢳⢕⢝⢜⢜
⢮⢳⡹⣪⢳⢝⢵⢕⢝⢜⢜⢜⠔⡅⠆⢕⠰⡐⡑⢌⠜⢜⠀⠀⠀⠀⠀⠀⠀⢠⢴⡯⣟⣷⣻⣺⡽⡕⡡⠊⡢⠑⠀⠕⡈⠄⢅⠑⠔⡐⠅⢍⢂⢊⠌⢌⠐⡐⡈⠢⡑⢜⢔⢕⠕⢅⢕⠱⡑⡑⠔⡈⢐⠡⠨⢂⣿⡷⣟⣯⡷⣿⣺⣟⣯⣯⡷⣟⣾⣿⢂⠇⢳⢹⢪⡣⡳⡹⡸⡱
⡯⣳⢝⢼⡸⡱⡱⡣⡣⡣⡊⢆⠣⠪⡘⢔⣑⣌⢌⠆⡃⡹⠀⠀⠀⠀⠀⠀⠀⢸⣯⢃⡽⣞⡷⣯⢿⡅⢂⠅⡂⠢⠠⡁⡂⠅⢂⠌⡂⠌⢌⢂⢂⠢⠈⠄⢂⠐⠨⢐⠡⢑⠌⡂⠅⢕⢐⠡⢂⠊⢔⠐⠄⢅⠅⢅⣿⢿⡽⣷⣟⣯⡷⣟⣷⢯⡿⣯⣟⣿⢌⠂⡂⠅⢢⡄⢅⠡⢉⠊
⢯⡪⣫⡣⡳⣕⢕⢅⢇⠪⡘⢌⢜⣼⢯⣯⢷⣫⢷⣳⢶⢼⠀⠀⠀⠀⠀⠀⠀⢸⣗⣌⢹⢽⢯⡯⣟⢆⢁⠂⠌⠨⢐⠐⠠⢁⢂⢐⠠⢁⢂⢂⢂⠂⠡⠈⠄⠨⠈⠄⡨⢐⢐⠨⠨⠐⢄⠑⠄⡑⠄⠅⠕⢐⢈⢐⣽⡿⣯⡷⣟⣷⣟⣯⣿⢽⣻⣷⣻⣿⢢⠂⡐⡈⠄⢯⡷⣇⢂⠢
⣇⢏⢎⢮⢹⢸⢱⢕⣥⣳⣺⢽⣻⣺⢽⢾⢽⣺⢯⡯⣟⢽⠫⠢⡄⡀⠀⠀⠀⢸⣗⣅⡾⣯⢾⠫⠋⠔⡀⡊⠨⢈⠐⡈⠌⡐⡀⠂⠌⡐⢀⢂⠂⠌⠠⠁⠌⡈⠌⢐⠐⡀⡂⡐⠡⡁⠢⢈⠢⠨⠨⠈⠌⠠⠠⠐⠸⡻⣿⢿⣯⣷⣿⢷⣿⢿⡿⣾⠿⠫⠘⢔⠔⠨⢈⠐⠝⣷⣐⠀
⡧⡳⡱⡕⣕⢵⢯⣻⣺⢞⣽⢽⣺⢽⢽⡽⣽⢽⡽⡪⡑⡐⡡⢑⢐⢑⠢⣄⢀⢸⣟⡾⣽⣝⡧⠨⢈⠂⡂⠄⠅⠂⡂⢂⠡⢀⠂⠡⢁⠐⡐⠠⠈⠄⠡⠈⠠⢀⠂⡁⢂⠂⠔⠠⢁⠂⠅⡂⠌⢂⠡⠁⠌⢐⠀⠅⢂⠨⢀⠑⣐⠬⡂⡑⡈⠅⡑⠥⠡⠡⠅⢊⠠⢁⠂⠌⡐⠠⠳⡅
⡳⡝⡵⣹⣞⣽⢽⣺⣳⣻⢾⢽⣺⢯⢯⡯⣗⢯⢣⢂⠆⡊⢄⠕⡐⡡⠊⢄⠕⡑⡑⢍⢈⠊⠍⠠⢁⠂⡐⠈⠄⠡⠐⡀⢂⠂⠌⠨⢀⠂⠄⠡⢈⠐⢈⠠⠁⠄⠂⡐⢐⠨⠈⠌⠠⠨⠐⠠⢁⠂⠄⠡⠈⠠⠐⢈⠠⠐⣠⢾⢊⠡⡐⠌⠆⡃⠌⠄⠡⠨⠐⡐⡐⢐⢈⢐⠠⠁⠅⠱
⡣⢕⣽⣳⢗⣯⣻⣺⡵⡯⡯⣟⡾⡽⣽⢾⢭⢣⢣⢂⢪⢐⠡⡂⡢⠊⢌⢂⡊⡔⢨⢸⠀⠄⠡⠈⠄⠂⠄⠡⠈⠄⡁⢐⠠⠈⠄⡁⠂⠌⡈⡐⠠⠈⠠⠐⠐⢈⠀⡂⠂⡂⠡⠈⡐⠠⠁⠡⠀⡂⠈⠄⠡⢈⣰⣰⣲⢽⠝⡙⠄⡁⢂⠡⢁⢐⠠⠁⠅⠌⡐⠠⢑⠄⠂⠄⢂⠡⢈⠂
⡑⣼⣗⡯⣟⣞⣞⣗⡯⣟⣽⡳⡯⣯⢷⢯⡇⡇⡇⣇⢇⠇⢍⠌⢌⠪⢘⠤⠱⡨⢊⠪⡐⡈⠄⢁⠂⡁⠌⠠⠁⢂⠀⡂⠠⠈⠄⠂⡁⢂⠐⠠⠈⠄⠡⠀⠅⠐⡀⠂⡁⠄⠂⡁⠄⠂⡁⠌⠠⠀⠅⡈⣴⣳⢗⡟⡘⠠⠁⠔⡐⢈⠔⡈⠄⡐⠠⠁⠅⢂⠂⡁⢢⢁⠪⡈⡄⡌⢔⢐
⣼⣟⡾⣝⡷⡽⣞⣷⢯⣗⡷⡯⣟⡵⡿⣽⣎⢎⢎⢎⠆⡑⡐⢅⠢⠡⡡⢊⢱⠨⢐⠡⢊⠔⡐⢀⠂⡀⢂⠨⠐⠀⡂⠐⡀⠡⢀⠡⠐⠀⠌⠠⠁⠌⡀⠅⠈⠄⠂⢁⠠⢀⠁⠄⢐⠀⢂⠠⠁⡈⢄⡾⣳⠫⢉⠂⡂⠡⢁⠕⣀⢃⢐⠠⠂⡂⠡⠡⠨⠐⡐⢌⠢⢂⢐⠠⠂⠌⠨⠈
⡿⣞⣯⢷⢯⢿⣽⢯⣟⡮⣯⢯⣗⡿⡽⣗⣷⢱⡱⡱⡁⠪⡐⡁⡪⠨⡐⠔⢌⠪⡐⡡⢂⠅⢕⠀⡐⠠⠐⠀⠌⠠⠐⢀⠂⡈⠠⠀⢂⠁⠌⠠⠁⡐⠀⠂⡁⠂⡁⠄⠂⡀⢂⠁⠄⡈⠄⠐⡀⢂⠌⢾⣝⡠⢂⠌⡄⢥⢑⡅⡆⢐⠠⢂⠡⠠⢁⢂⢅⢕⠘⠠⢁⢂⠡⠠⠡⠨⠈⠔
⣿⣻⣽⣟⡿⣯⣟⣯⣷⣻⢵⣻⢮⣟⣯⢿⣯⡧⡫⡪⡐⡅⡖⡑⠔⡡⠊⡌⡢⢡⠢⡨⠢⡑⡒⡂⢆⠢⣈⠐⢈⠠⠈⠠⠀⠂⠄⠡⠀⡂⠈⡄⡢⢠⢡⢁⢀⠂⠄⠂⠁⠄⠂⠠⠁⠠⢀⠡⠠⡁⣎⡾⡃⠅⢂⠂⡂⠌⠢⡣⠂⡂⠌⡐⠠⡡⢢⠱⠈⠄⠌⠨⢀⢂⢄⢅⠎⠢⠃⠅
⣿⡽⣾⣳⣟⡿⣞⣿⣞⣯⣟⢾⢽⣺⣺⢯⣷⢿⣺⢸⢰⢕⠕⡨⡨⢐⠅⡊⠔⡐⠅⢅⠕⡐⢔⠨⢂⠅⡢⢑⠔⠢⢌⢄⢅⠬⠰⠨⡒⠌⠪⡐⢌⢢⢂⢂⠢⠑⡄⠁⠌⠠⠈⠄⡁⠌⠀⡌⢂⡂⣓⠇⡂⢌⢐⠐⠠⠨⢈⢎⢆⢆⢅⠢⡣⢊⠂⠌⠄⢅⢪⠸⢐⠡⠁⢆⠌⠄⡑⡈
⣿⡽⣯⢿⣞⡿⣯⣷⣟⡷⣯⢯⣟⢾⣺⢽⣞⣿⣻⡸⡸⡸⡐⢌⠢⠡⡂⠪⡈⡢⠡⡑⡐⢌⢂⠪⡐⠌⠔⡂⡣⢉⠢⡑⡐⠌⠜⡨⢐⠡⡑⢌⠔⢅⠢⡢⠥⡡⠐⢑⡈⠠⠁⡐⠀⠄⡱⠐⡐⢰⡺⢁⠐⡐⠠⠨⢈⢐⢐⢕⡑⡌⡊⢎⠔⠠⠨⠠⡑⡕⢐⠈⠄⢂⠡⠨⡐⢐⠠⠂
⣿⣽⣟⣯⡿⣽⣻⣞⣷⣟⣯⢷⢯⣻⣺⢽⣳⢯⢯⡷⣕⡕⡕⡅⢕⠡⡪⡈⡂⡢⢑⢐⢌⢂⡢⠡⡂⠕⡡⢊⠄⡅⠕⡐⠌⠜⡌⠔⡁⡊⢄⠕⡸⠨⡨⡂⠅⠕⡌⠠⢺⣲⡅⡢⢉⠌⠄⡑⠰⣫⡯⡂⢐⠠⠡⠈⠄⢂⢜⠆⡕⢬⢊⢌⠎⡕⡨⡐⢅⠇⢐⠈⠄⡁⡂⢅⢆⢂⠢⢁
⣿⣺⢷⣯⣟⣯⡿⣞⣷⣻⡽⣽⢽⣺⢽⢽⣺⢽⣫⡯⣗⣟⣎⢎⢐⢑⠜⡸⢸⠰⠱⡑⠍⢌⢂⠕⡈⡢⢊⢌⢢⠨⡢⠪⠨⢊⢎⢌⡂⡊⡢⡃⢎⠪⡐⠌⡣⡑⡸⢬⡻⡮⡇⡐⠠⡁⡂⡂⠡⢈⢾⠂⠡⠠⠡⠨⡈⡆⡇⡕⠜⡌⡆⡢⡡⡈⢆⠪⡪⡨⡠⢨⠰⢈⢐⠠⠱⠐⡈⠄
⣯⣿⣻⢾⡽⣷⣻⣯⣟⡷⡯⣗⣯⢯⢯⣟⣞⡯⣗⡯⣗⣯⢾⡸⢌⠢⠨⢂⠢⡡⠕⠌⢌⢂⠢⢊⠔⡘⡐⢅⢢⢑⠬⡸⡸⡸⣸⢔⢕⢱⠰⡘⢄⠅⢕⢑⠔⡕⡈⣗⢯⡯⡃⠄⠡⢐⠈⠌⡈⢄⢺⢌⢌⢆⢕⢕⢱⠘⢀⠪⡊⡢⡑⡅⡣⡊⢎⢌⢊⢆⠪⡂⠌⡀⡂⠄⠅⡅⠂⠌
⣿⣞⣯⣿⣻⣽⢷⣻⡾⡽⣽⡳⡯⣯⣻⣺⣺⢽⡳⡯⣟⢾⢽⣪⡕⣌⢪⢰⢡⢢⢅⢇⡕⣔⢕⢕⢜⢔⢕⢕⢕⠵⠩⢃⠋⡊⠨⠈⠢⡓⢜⠸⣐⢑⢅⢑⡅⢮⣢⢯⡗⡃⠄⠅⠣⠒⠌⠆⠆⡃⢌⢆⠣⡑⠆⠕⢁⢈⠠⢀⠘⢔⡑⢬⠨⡊⢆⠕⡌⢜⢌⢆⢂⠂⠄⠅⣂⣊⡬⣔
⣷⣟⣷⣻⣾⣽⣻⣗⣯⢯⣗⣯⢯⣗⣗⣯⢾⢽⢽⣫⡯⡯⣟⡾⣽⣺⣝⣗⠇⠣⢣⢣⢣⢣⢣⠣⠣⠃⡑⢀⠂⠐⡈⠠⠐⢀⠂⡁⢂⠨⠈⠍⡂⠣⠪⠊⠌⡉⠚⡙⠌⢆⠪⡠⠡⢡⢡⢑⢔⠸⡰⡂⢇⠡⠁⠌⠠⢀⠐⡀⠂⠄⠨⠘⢌⢪⠠⢑⢜⠰⡑⣌⢦⢵⢕⢯⢚⢎⠪⠢
⣿⣞⣯⣷⢷⣯⣷⣻⣺⢽⣺⢾⢽⣺⡵⡯⡯⣟⡽⣞⣽⢽⣳⣻⣺⣺⣺⢾⡡⢁⠂⠄⢂⠐⠠⠐⡀⠅⡀⢂⠨⠀⡂⠄⠡⠐⢀⠐⠠⠐⢀⠡⠀⠌⠠⠁⡂⠄⠡⠀⡂⠄⡑⠘⢌⢢⢂⠅⡕⢍⠢⠃⡐⠀⠅⠨⠐⡀⠂⢄⠡⠨⠠⢁⢑⢅⠎⢤⢱⣕⢽⠪⠫⡡⢃⠕⣐⣢⡱⣕
⠷⡻⡳⢻⢫⢷⢻⢺⢾⢽⣳⣻⢽⣺⡽⣽⣫⢷⣻⢽⣺⣽⣺⣵⣻⣺⣺⣽⠐⠄⢌⢐⠠⢈⠐⡀⠂⠄⢂⠐⡀⠡⠀⢂⠁⠌⠠⢈⠐⢈⠠⠐⠈⠄⡁⡂⡐⠈⠄⡁⡂⠅⡂⡑⡐⠠⠨⢈⠊⠡⠈⠄⠂⡁⠌⠠⢁⠂⢅⢂⠌⠄⢅⠢⠨⡢⡗⡏⢇⢣⢑⢕⣱⡸⣴⡫⣞⣞⢮⢗
⡽⡾⣝⣯⢣⣗⣗⢵⡲⣕⢥⢍⡫⠳⢯⣗⡯⣟⡾⣽⣳⣳⣳⣳⢗⣯⢾⣺⢨⠨⡐⡀⡂⢂⠂⢂⠡⠈⠄⠂⠄⠅⠅⡂⠄⠡⢈⠠⢈⠠⠐⡈⠄⠡⢀⠂⠄⠅⢂⢐⠠⢑⢐⠐⢌⠨⠐⠠⠈⠄⠡⠨⠐⠠⢈⠐⠠⠨⢐⠐⡅⢕⢐⠅⠕⣍⠪⣨⣢⣳⢽⣝⢮⢯⢾⣺⢗⡯⡯⡯
⢋⢏⢍⢎⢎⢊⠌⡃⡛⡪⢏⣗⢽⢵⣲⠨⡙⠳⡯⣗⣷⣫⢾⢽⣽⣺⡽⡎⡆⡣⢂⢢⠨⠂⠌⡀⢂⠡⠈⢌⠜⡌⡪⠠⠡⢁⠂⡐⠠⠠⢁⠂⠌⢌⢐⠨⠐⡁⡂⢕⢨⢐⢄⢑⢐⠨⠈⠌⠨⢈⠄⠅⢅⠕⡐⢌⠨⠐⠠⠡⠨⡘⡐⡅⢕⡼⣺⣕⢷⢵⣫⢞⡽⡽⡵⣫⢯⢯⣻⣺
⢸⢨⢪⢢⠣⠢⠪⠰⡐⡔⡐⠄⠍⡣⠣⣸⡺⣕⡌⡓⣷⣫⢿⢽⣺⣺⢽⠪⣊⢢⢱⠨⡨⡨⢂⠌⡀⡂⢅⢕⠱⡨⠪⡘⠨⢀⢂⠐⡈⢐⠄⠅⠕⡐⡐⠨⢐⠐⠠⡑⡜⢔⢢⠱⡐⠅⢅⢅⢑⢐⢌⢊⠢⡑⡌⢆⢅⠅⢕⠨⠨⢐⠔⡘⡘⣞⣵⣳⣫⢷⢽⢝⡾⣝⡽⡽⣝⣽⣺⣺
⡸⡸⡸⡨⡨⠨⡊⢌⢂⢢⠡⡡⢑⠄⠕⡨⢊⢗⡽⣲⡨⠺⡯⣯⢷⢯⡣⡫⣢⢣⢣⢱⢑⠌⡂⡂⢂⠢⡑⢔⢑⠬⡑⠌⠌⠄⡂⢐⢀⢂⠪⠨⡊⢔⠨⠨⡐⠨⠐⢌⢌⢎⠢⡣⡱⡑⢅⠆⡕⢅⢢⢡⢑⠱⡘⡌⢆⢣⢱⠨⡊⡢⢨⠨⡪⣗⢷⢵⣳⣫⢯⢯⢞⣗⢯⣟⢾⣺⢾⣺
⢸⢸⢘⠔⡨⠨⡂⢅⠢⡊⡂⡪⢐⠌⢌⢂⠢⡑⢍⠺⣪⢧⢙⢽⡽⣣⡳⣝⢜⡜⡜⠜⢄⠕⡐⡨⢠⢱⠪⡨⢢⢣⠡⠡⠡⠡⢐⠀⡂⠔⡡⢑⠌⡢⠡⡑⢌⠌⢌⠢⡱⡱⡱⡱⡱⡱⡱⡱⡘⢔⢑⢌⠢⢣⢑⢜⠸⡨⢢⠣⡱⢌⠆⡵⣝⣗⢯⣗⢷⢽⢵⢯⣻⡺⣝⡮⣟⢮⣻⣺
"

sleep 2

npm init -y

npm pkg set type=module
npm pkg set main=./src/server.ts
npm pkg set scripts.dev="tsx --watch ./"

cat <<'EOF' > tsconfig.json
{
  // Visit https://aka.ms/tsconfig to read more about this file
  "compilerOptions": {
    "rootDir": "./src",
    "outDir": "./build/src",
    "baseUrl": "./src",
    "paths": {
      "@/*": ["*"]
    },
    "ignoreDeprecations": "6.0",
    "strict": true,
    "allowJs": false,
    "pretty": true,
    "skipDefaultLibCheck": false,
    "strictFunctionTypes": true,
    "strictNullChecks": true,
    "skipLibCheck": false,
    "moduleDetection": "force",
    "noUncheckedSideEffectImports": true,
    "resolveJsonModule": true,
    "removeComments": true,
    "noUnusedParameters": true,
    "noUnusedLocals": true,
    "noStrictGenericChecks": false,
    "noImplicitThis": true,
    "noImplicitReturns": true,
    "noImplicitAny": true,
    "forceConsistentCasingInFileNames": true,
    "esModuleInterop": true,
    "allowSyntheticDefaultImports": true, //Alterado pq está dando error no import do fs
    "noFallthroughCasesInSwitch": true,
    "noErrorTruncation": true,
    "noEmitOnError": true,
    "noEmitHelpers": true,
    "noEmit": false,
    "declaration": false,
    "exactOptionalPropertyTypes": true,
    "maxNodeModuleJsDepth": 0,
    "moduleResolution": "node",
    "lib": ["ES2023"],
    "module": "commonjs",
    "target": "ES2023",
    "types": ["node"],
    "typeRoots": ["./src/types", "./node_modules/@types"]
  },
  "exclude": ["node_modules", "./build"],
  "include": ["src/**/*"]
}
EOF

cat <<'EOF' > LICENSE
MIT License

Copyright (c) 2026 [fullname]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
EOF

cat <<'EOF' > README.MD

![Node+Typescript](https://i.imgur.com/yrV7Go3.jpeg)

# 🏷️ Sistema de Leilão em Tempo Real

Estou desenvolvendo um sistema de **Leilão em Tempo Real** utilizando a stack:

- **Node.js**
- **TypeScript**
- **Express**
- **Mongoose (MongoDB)**
- **React**
- **Socket.io**

---

## 📌 Regras de Negócio Principais

### ⏳ Sistema de "Overtime" (Anti-Sniping)

Se um lance for feito **nos últimos 10 segundos**, o cronômetro do leilão deve **resetar para 10 segundos restantes**.

- Essa regra pode acontecer **sucessivamente**.
- Deve ser validada **no backend**.
- A atualização deve ser enviada para todos os clientes via **Socket.io**.

---

### 💰 Preço Inicial

- O leilão deve começar obrigatoriamente pelo `initialPrice` definido pelo dono do item.
- Nenhum lance pode ser menor que o valor atual.
- O primeiro lance válido deve respeitar o `initialPrice`.

---

### 🔨 Sistema de Lances

O sistema deve aceitar:

- Botões de incremento fixo:
  - `+5`
  - `+10`
  - `+50`
- Campo de **Lance Personalizado (input)**

Regras:

- O valor do lance deve ser **maior que o lance atual**
- Validação deve acontecer **no backend**
- Nunca confiar apenas na validação do frontend

---

### ⚡ Atualização em Tempo Real

Deve utilizar **Socket.io** para:

- Atualizar o cronômetro para todos os usuários
- Atualizar o valor atual do lance
- Notificar quando houver novo maior lance
- Notificar quando o leilão finalizar

---

## 🎯 O Que Eu Preciso Agora

[INSIRA AQUI O QUE VOCÊ QUER, EX:  
"Crie o AuctionSchema e o evento do Socket.io que escuta o lance, valida o valor mínimo e aplica a regra de extensão de 10 segundos."  
OU  
"Crie um componente React chamado BidPanel que receba o lance atual via props, tenha os botões de incremento e um input para lance personalizado com validação."  
OU  
"Mostre como sincronizar o relógio do servidor com o componente de Countdown do React para evitar atrasos."]

---

## 📌 Requisitos Técnicos

- Utilizar **boas práticas de TypeScript**
- Separar interfaces
- Garantir segurança dos dados no lado do servidor
- Nunca confiar apenas na validação do frontend
- Aplicar tipagem forte nos eventos do Socket.io
- Manter o código organizado por responsabilidade

---

## 💡 Dicas de Como Usar Esse Prompt

### 🔹 Para o Backend

No campo final entre colchetes, peça:

> "Crie o AuctionSchema e o evento do Socket.io que escuta o lance, valida o valor mínimo e aplica a regra de extensão de 10 segundos."

---

### 🔹 Para o Frontend

Peça:

> "Crie um componente React chamado BidPanel que receba o lance atual via props, tenha os botões de incremento e um input para lance personalizado com validação."

---

### 🔹 Para Sincronização de Tempo

Peça:

> "Mostre como sincronizar o relógio do servidor com o componente de Countdown do React para evitar atrasos."

---

🚀 Objetivo: Construir um sistema de leilão profissional, seguro, escalável e 100% sincronizado em tempo real.
EOF

cat <<'EOF' > .npmrc
save-exact=true
fund=false
package-lock=false
init-license=Apache 2.0 
init-author-name=
EOF

cat <<'EOF' > .prettierrc
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": false
}
EOF

cat <<'EOF' > .env
PORT=3000
JWT_SECRET=
MONGO_URI=mongodb://127.0.0.1:27017
MONGO_NAME=
EOF

cat .env

cat <<'EOF' > .env.example
PORT=****
JWT_SECRET=****
MONGO_URI=mongodb://127.0.0.1:27017
MONGO_NAME=****
EOF

cat <<'EOF' > .gitignore
node_modules
.env
EOF

cat .gitignore

npm i express bcryptjs jsonwebtoken mongoose mongodb zod multer helmet express-rate-limit body-parser cors \
cookie-parser remove-accents stripe tsc-alias nodemailer node-cron morgan dotenv compression sharp vitest

npm i -D eslint typescript tsx @types/nodemailer @types/node-cron @types/node @types/multer @types/jsonwebtoken \
@types/express @types/cors @types/cookie-parser @types/compression @types/body-parser @types/bcryptjs @types/morgan @types/dotenv

mkdir -p src build

cd src

touch server.ts

echo 'console.log("Tudo OK")' >> server.ts

mkdir -p routes controllers models config database test utils middleware zod types uploads logs docs

cd routes
mkdir v1

cd ../..

echo "✅ Setup concluído com sucesso!"
echo "👉 Rodando...: npm run dev"

sleep 2

npm run dev
```
