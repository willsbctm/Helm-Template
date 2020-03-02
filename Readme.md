## Template Go

#### Espaços entre textos
`-` Remove o espaço entre o parâmetro e o texto

Cosidere a expressão: 
```
" {{ 100 }} > {{ 87 }} " 
```
Imprime:
```
" 100 > 87 "
```

Agora com:
```
" {{- 100 }} > {{- 87 -}} " 
```
Imprime:
```
"100 >87"
```

#### Variável
```
{{ $nomeDaVariavel := "1234" }}
O valor é {{ $nomeDaVariavel }}
```

#### Range

Só valor:
```
{{ range $valor := Valores }}
Iteração do valor {{ $valor }}
{{ end }}
```
Propriedade e valor:
```
{{ range $propriedade, $valor := Valores }}
Iteração do valor {{ $valor }} da {{$propriedade}}
{{ end }}
```

#### Include
Adiciona um template ao arquivo atual:
```
{{ include "template" . }}
```