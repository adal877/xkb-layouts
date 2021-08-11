# xkb-layouts
Essas são as minhas versões de alguns layouts de teclados

## Vantagens
- [ Duvído que seja ] Ergonomico                  
- [ Talvez ]          Pratico                     
- [X]                 Tem os ascentos brasileiros 

## Layouts
* Dvorak. Original: https://www.dvorak-keyboard.com/
* Workman. Original: https://workmanlayout.org/#introducing-the-workman-keyboard-layout
* Halmak. Original: https://github.com/MadRabbit/halmak

## Configuração
1. Encontre o diretorio `xkb/symbols/`
2. Execute: `sudo cp [layout] [xkb/symbols/]`
3. Agore só execute: `setxkbmap -model abnt2 -layout [layout] -option "shift:both_capslock"`

(Mais a baixo vou explicar o porque do `-option "shift:both_capslock"`)

Esse é um meio simples de configurar um novo layout de forma *NÃO PERMANENTE*

Mais informações, exemplos e explicações detalhadas (em inglês): 
[Xkb Linux](https://medium.com/@damko/a-simple-humble-but-comprehensive-guide-to-xkb-for-linux-6f1ad5e13450)

## Detalhes e Informações

O acesso às taclas funcionam da seguinte forma:
* Primeira camada: 
  * São os caracteres acessados sem o uso de outras teclas como shift, ctrl, alt e suas combinações...
* Segunda camada:
  * `Shift`
* Terceira camada:
  * `Alt-gr`

Todos os layouts possuem as seguintes teclas:

1. `key <CAPS>   { [                   Super_L                    ] };`

   Tecla CapsLock como `Super`
   
  (Por isso o `-option "shift:both_capslock"` para usar ambos os Shifts como CapsLock)
  
2. `key <ESC>    { [     ccedilla,        Ccedilla                ] };`

   Tecla Esc como `ç` e `Ç`
   
3.
* Dvorak:
  * `key <AC01>   { [            a,               A,          Left ] };`
  
  * `key <AC02>   { [            o,               O,          Down ] };`
  
  * `key <AC03>   { [            e,               E,            Up ] };`
  
  * `key <AC04>   { [            u,               U,         Right ] };`
  
* Workman:
  * `key <AC01> { [            a,              A,          Left  ] };`
  
  * `key <AC02> { [            s,              S,          Down  ] };`
  
  * `key <AC03> { [            h,              H,            Up  ] };`
  
  * `key <AC04> { [            t,              T,         Right  ] };`
  
* Halmak:
  * `key <AC01> { [           s,             S,           Left ] };`
  
  * `key <AC02> { [           h,             H,           Down ] };`
  
  * `key <AC03> { [           n,             N,             Up ] };`
  
  * `key <AC04> { [           t,             T,          Right ] };`
  
As teclas à esquerda, na linha central, funcionam como os direcionais com o uso da tecla Alt-gr.
  
Com o comando: `echo 'File:line: match'; grep -nrw 'b,'` é possível ver as teclas `b` que estão nas mesmas posições entre os layouts.
Faça o mesmo para as demais teclas. 

*ATENÇÃO*
* É recomendavel executar o comando abaixo para ver demais modificações com as barras:  
  `echo 'File:line: match'; grep -nrw '\(back\)\?\(slash\|bar\)'`
 
 <strike>da teus pulos para fazer as modificações para as demais teclas</strike>

# Muito thanks
  
Seguinte seres, qualquer ideia, sugestão e ou reclamações é só abrir um issue.
tmj <3
![alt text](https://68.media.tumblr.com/06ea570b99b4e449c5aebeec2c5b6e75/tumblr_oldiimQp4Z1va5dgko1_500.png)
