# desafio1hc3

Delivered-To: oarthurcandido@gmail.com
Received: by 2002:a05:6a10:4411:0:0:0:0 with SMTP id s17csp36892pxu;
        Wed, 25 May 2022 18:20:34 -0700 (PDT)
X-Google-Smtp-Source: ABdhPJwtKJiAIf7Nigv4Xkrn9AnASzbwuIYZflmoSznHpX+c4yWlO8vVt7lhR07y+1Acj23pa0xE
X-Received: by 2002:a05:6808:2391:b0:32b:9d77:84b7 with SMTP id bp17-20020a056808239100b0032b9d7784b7mr3347956oib.280.1653528033833;
        Wed, 25 May 2022 18:20:33 -0700 (PDT)
ARC-Seal: i=1; a=rsa-sha256; t=1653528033; cv=none;
        d=google.com; s=arc-20160816;
        b=XLSyITCR31iMvV4aUH2N6a2XvriTW4IuTdc6L5zsiKRatr+TW5BVxPGnDRM3cKHWe/
         DI22+x0RXW/LOBapFVFXMnGQbSY7nUg9zFqNoD2CS5OAWu0q9h0jH5YNlyA7uDlEqTHX
         U/ht/3T9a6KTpa8y0ysJgDMfWDqywObirc7HFkeFZJHaQTh65BMdc4FGNdAyZD//DqWL
         9VP05gKMXAIwqpqWB1WTA67YMgTTTNVSsroQHRQl+NvJCihD6dGZug+G2aYik7tHHPD/
         Yr1QbR9KKb+ThHMXE4zHMe2+tHWteNBWRy/1lWA6t2MECGhEmFcgssQfuJf3av/FthgR
         GMig==
ARC-Message-Signature: i=1; a=rsa-sha256; c=relaxed/relaxed; d=google.com; s=arc-20160816;
        h=content-transfer-encoding:from:subject:reply-to:to:date
         :mime-version:message-id:sender:dkim-signature:dkim-signature;
        bh=7kgvukFmiuVALwIj/21eT1mdkTPXFVLa+Q8jneCCRPU=;
        b=Tub/GBpM2C35lWcNVUS6o3x4tIVNmw16sSVmUhbhyLC1f+ecK97iq7bw0KSil/4/No
         AxINl5RAdNkO527JKxtjSrlL2RlLeNySuR1unvr2wBD5VoyxX/3aIq0vLNBWUfcbNad0
         9D3FNZg1sKZ9e5Yy48bQRV4MnfWNIehcV7sTwLvflmqLvPoPlQT1L8jAd4FIuCJKzfPk
         tXJBJ2oz0+/O89cyKLATecdgxMZ3KAVBemf/PnJqLeHHAt4uu6LoFn4eAwL7iZ+kAszt
         xoML9qxb3MuSDlvzkZc6EG1ICNUTSrKO6P/7+AC8aKxaK6X/IJ4ZPdxAmZGsH7YYlwym
         wbiw==
ARC-Authentication-Results: i=1; mx.google.com;
       dkim=pass header.i=@typeform.com header.s=krs header.b=s6+RFRAP;
       dkim=pass header.i=@mailgun.org header.s=mg2 header.b=QuW6k23B;
       spf=pass (google.com: domain of bounce+0e3685.a82fe-oarthurcandido=gmail.com@typeform.com designates 159.135.229.11 as permitted sender) smtp.mailfrom="bounce+0e3685.a82fe-oarthurcandido=gmail.com@typeform.com";
       dmarc=pass (p=REJECT sp=REJECT dis=NONE) header.from=typeform.com
Return-Path: <bounce+0e3685.a82fe-oarthurcandido=gmail.com@typeform.com>
Received: from m229-11.mailgun.net (m229-11.mailgun.net. [159.135.229.11])
        by mx.google.com with UTF8SMTPS id p5-20020a4a95c5000000b0040e751ce971si306042ooi.23.2022.05.25.18.20.21
        for <oarthurcandido@gmail.com>
        (version=TLS1_3 cipher=TLS_AES_128_GCM_SHA256 bits=128/128);
        Wed, 25 May 2022 18:20:33 -0700 (PDT)
Received-SPF: pass (google.com: domain of bounce+0e3685.a82fe-oarthurcandido=gmail.com@typeform.com designates 159.135.229.11 as permitted sender) client-ip=159.135.229.11;
Authentication-Results: mx.google.com;
       dkim=pass header.i=@typeform.com header.s=krs header.b=s6+RFRAP;
       dkim=pass header.i=@mailgun.org header.s=mg2 header.b=QuW6k23B;
       spf=pass (google.com: domain of bounce+0e3685.a82fe-oarthurcandido=gmail.com@typeform.com designates 159.135.229.11 as permitted sender) smtp.mailfrom="bounce+0e3685.a82fe-oarthurcandido=gmail.com@typeform.com";
       dmarc=pass (p=REJECT sp=REJECT dis=NONE) header.from=typeform.com
DKIM-Signature: a=rsa-sha256; v=1; c=relaxed/relaxed; d=typeform.com; q=dns/txt; s=krs; t=1653528033; h=Content-Transfer-Encoding: Content-Type: From: From: Subject: Subject: Reply-To: To: To: Date: Mime-Version: Message-Id: Sender: Sender: X-Feedback-Id; bh=7kgvukFmiuVALwIj/21eT1mdkTPXFVLa+Q8jneCCRPU=; b=s6+RFRAP1WTERni60pGcXdvOmcoQF9ibUVTh4JmFhV3fQGtBmCiDTgkTznTXkUweCZfItrTR JHKOMYEO+c997+Mqtorrjv8R86LjdM13L2tFzsjupi2rIWS/+TLZ02ByJWqsGbLr2SbyzHeR WMjS7EjZTEQH+BmymizGTJBXus8=
DKIM-Signature: a=rsa-sha256; v=1; c=relaxed/relaxed; d=mailgun.org; q=dns/txt; s=mg2; t=1653528033; h=Content-Transfer-Encoding: Content-Type: From: From: Subject: Subject: Reply-To: To: To: Date: Mime-Version: Message-Id: Sender: Sender: X-Feedback-Id; bh=7kgvukFmiuVALwIj/21eT1mdkTPXFVLa+Q8jneCCRPU=; b=QuW6k23BF0yL3v1p7xoMjD1w20G8+Z4naWK+RDjqiS3nXs+FCKdYPdOp62wr2WEVsJrdt10m 841VVkbKmigTKvJGSuAm7cQJjga2CKMSurcHlRfBluk0e88fSku7dmCkt0MvJQQ09FqhRs+x T42YO3l1xcHScWScOsCnCuSQdsA=
X-Feedback-Id: 5a25579afa60952bd42dc766:mailgun
X-Mailgun-Sending-Ip: 159.135.229.11
X-Mailgun-Sid: WyJhMGYyMSIsICJvYXJ0aHVyY2FuZGlkb0BnbWFpbC5jb20iLCAiYTgyZmUiXQ==
Received: from localhost (ec2-34-230-177-131.compute-1.amazonaws.com [34.230.177.131]) by smtp-out-n03.prod.us-east-1.postgun.com with SMTP id 628ed5bc00780398288a2cbb (version=TLS1.3, cipher=TLS_AES_128_GCM_SHA256); Thu, 26 May 2022 01:19:56 GMT
Sender: notifications@typeform.com
Message-Id: <20220526011956.16f0f357aa1edfad@typeform.com>
Mime-Version: 1.0
Date: Thu, 26 May 2022 01:19:56 +0000
To: oarthurcandido@gmail.com
Reply-To: corp@gama.academy
Subject: Aqui está o resultado do Hiring Coders #03 - Desafio #01. 
X-Mailgun-Variables: {"form_uid":"U4DZln0N", "tracking_id":"708359168d63fd0d05d2a821c925ccc9"}
From: notifications@typeform.com
Content-Type: text/html; charset="utf-8"
Content-Transfer-Encoding: quoted-printable

Heeey, Arthur Candido! <br/>Tudo bem?<br/><br/>Sua nota final no Desafio #0=
1 do Hiring Coders #03 foi: 11 de 13 quest=C3=B5es!<br/><br/><strong>INFORM=
A=C3=87=C3=95ES IMPORTANTES:</strong><br/>*S=C3=B3 consideraremos a sua pri=
meira resposta a este formul=C3=A1rio, uma vez que o gabarito do desafio es=
t=C3=A1 abaixo. Portanto, nada de tentar fazer de novo, ok?<br/>*O peso des=
se desafio no ranking ser=C3=A1 20;<br/><br/>Aqui est=C3=A1 o resultado do =
seu desafio:<br/><strong>1. Considerando o c=C3=B3digo JavaScript a seguir,=
 qual ser=C3=A1 o output do alerta?</strong><br/>[...]<br/>Sua resposta: 01=
3<br/><strong>Resposta correta: 013</strong><br/><br/><strong>2. Considere =
o comando JavaScript a seguir.</strong><br/>document.getElementById('demo')=
.innerHTML =3D Date()<br/><strong>Numa p=C3=A1gina web na qual esse c=C3=B3=
digo seja aplicado, o elemento que =C3=A9 compat=C3=ADvel com a estrutura d=
o comando para receber a data corrente =C3=A9:</strong><br/><br/>Sua respos=
ta: &lt;p id=3D&#34;demo&#34;&gt;H&lt;/p&gt;<br/><strong>Resposta correta: =
< p id=3D"demo">H</p ></strong><br/><br/><strong>3. Analise o script JS a s=
eguir:</strong><br/>[...]<br/><strong>O resultado da execu=C3=A7=C3=A3o des=
se c=C3=B3digo =C3=A9:&nbsp;</strong><br/><br/>Sua resposta: 1/2/3/4/5/<br/=
><strong>Resposta correta: 1/2/3/4/5/ </strong><br/><br/><strong>4. Na ling=
uagem JavaScript, ao invocar o m=C3=A9todo getElementsByClassName, do objet=
o document, ser=C3=A1 retornado:</strong><br/><br/>Sua resposta: Um objeto<=
br/><strong>Resposta correta: Um array</strong><br/><br/><strong>5. Conside=
re o seguinte c=C3=B3digo JavaScript:</strong><br/>[...]<br/><strong>Ao fin=
al da execu=C3=A7=C3=A3o, quais valores ser=C3=A3o impressos?</strong><br/>=
<br/>Sua resposta: A,B,A,B,B.<br/><strong>Resposta correta: A,B,A,B,B. </st=
rong><br/><br/><strong>6. Considere o seguinte c=C3=B3digo JavaScript:</str=
ong><br/>let o =3D {one:1,two:2,three:3};<br/>for(let p in o) console.log(p=
);<br/><strong>Ao final da execu=C3=A7=C3=A3o, quais valores ser=C3=A3o imp=
ressos?</strong><br/><br/>Sua resposta: &#39;one&#39;, &#39;two&#39;, &#39;=
three&#39;<br/><strong>Resposta correta: 'one', 'two', 'three'</strong><br/=
><br/><strong>7. Em JavaScript, o operador new cria e inicializa um novo ob=
jeto.</strong><br/><strong>Qual operador N=C3=83O representa a cria=C3=A7=
=C3=A3o de um objeto de tipo nativo JavaScript?</strong><br/><br/>Sua respo=
sta: var l =3D new ArrayList();<br/><strong>Resposta correta: var l =3D new=
 ArrayList();</strong><br/><br/><strong>8. Analise os extratos de uma p=C3=
=A1gina Web incluindo o c=C3=B3digo JS exibido a seguir. Qual ser=C3=A1 o v=
alor no elemento de id=3D=E2=80=9Cbox=E2=80=9D ap=C3=B3s a opera=C3=A7=C3=
=A3o?</strong><br/>[...]<br/>Sua resposta: Valores DE CD BC AB<br/><strong>=
Resposta correta: Valores DE CD BC AB</strong><br/><br/><strong>9. Analise =
a p=C3=A1gina Web a seguir, escrita em (HTML) e com a linguagem JavaScript.=
</strong><br/> [...]<br/><strong>Como pode ser observado, uma fun=C3=A7=C3=
=A3o foi criada para ordenar os candidatos do array =E2=80=9Caprovados=E2=
=80=9D, considerando como crit=C3=A9rio de ordena=C3=A7=C3=A3o nota e idade=
. Ao executar este script no navegador Google Chrome, vers=C3=A3o 64, pergu=
nta-se: qual candidato ficou em segundo lugar?</strong><br/><br/>Sua respos=
ta: Jo=C3=A3o Oliveira<br/><strong>Resposta correta: Jo=C3=A3o Oliveira</st=
rong><br/><br/><strong>10.</strong> <strong>Analise o c=C3=B3digo JavaScrip=
t abaixo.</strong><br/> [...]<br/><strong>No navegador Mozilla Firefox, dad=
o o c=C3=B3digo acima, qual =C3=A9 a mensagem que aparece no console de err=
o?</strong><br/><br/>Sua resposta: Uncaught SyntaxError: Unexpected token I=
LLEGAL.<br/><strong>Resposta correta: SyntaxError: unterminated string lite=
ral.</strong><br/><br/><strong>11. Imagine o seguinte cen=C3=A1rio: Marcelo=
 lhe deve um dinheiro e promete pagar em parcelas mensais de R$ 70; com o i=
ntuito de prever qual seria o valor devido ap=C3=B3s o decorrer de 12 meses=
, voc=C3=AA resolve escrever algumas linhas de c=C3=B3digo (JavaScript). Le=
vando em considera=C3=A7=C3=A3o que o valor devido por Marcelo era de R$ 14=
00, qual seria o total devido ap=C3=B3s a execu=C3=A7=C3=A3o do trecho a se=
guir?</strong><br/> [...]<br/><br/>Sua resposta: Marcelo teria pago 840 rea=
is e lhe deveria ainda 560.<br/><strong>Resposta correta: Marcelo teria pag=
o 840 reais e lhe deveria ainda 560.</strong><br/><br/><strong>12. Consider=
e o fragmento de programa JavaScript abaixo.</strong><br/> var str =3D "123=
456789";<br/>var p =3D /[^5-7]/g;<br/>var resultado =3D str.match(p);<br/> =
<strong>A vari=C3=A1vel resultado vai conter:</strong><br/><br/>Sua respost=
a: 1,2,3,4,8,9<br/><strong>Resposta correta: 1,2,3,4,8,9</strong><br/><br/>=
<strong>13. Considere a p=C3=A1gina HTML abaixo, que cont=C3=A9m c=C3=B3dig=
o JavaScript.</strong><br/> [...]<br/><strong>Sabendo que com HTML DOM, Jav=
aScript pode acessar e mudar os elementos de uma p=C3=A1gina web, para que =
o Terceiro Par=C3=A1grafo seja adicionado ao cont=C3=AAiner identificado co=
mo caixa, a lacuna I deve ser corretamente preenchida por:</strong><br/><br=
/>Sua resposta: element.appendChild(para.appendChild(node))<br/><strong>Res=
posta correta: element.appendChild(para.appendChild(node))</strong><br/><br=
/>Abra=C3=A7os,<br/><strong>Bruce da Gama Academy <3</strong><br/><span sty=
le=3D'color:white'>dgtlux6hv55sf0sx9ajdgtluyttq7a5n</span><p style=3D"color=
:#AAAAAA; font-family:sans-serif; font-size:10pt;">A Typeform enviou este e=
-mail em nome de um criador da Typeform. N=C3=B3s n=C3=A3o somos respons=C3=
=A1veis pelo seu conte=C3=BAdo. Caso suspeite de abuso, como links suspeito=
s, denuncie-o <a href=3D"https://www.typeform.com/help/report-abuse/">aqui<=
/a>.</p>
<br>
<a href=3D"https://email.typeform.com/u/eJwdjrsOgzAMAL-mGZFtSEiGDJU6d-vSBRm=
bQFQeVQRD_76060l3Oo3sKQ0mRwIisOQAMVhXoUuQatsy46CJ9dLA_nkPaStLJdtipth7rRlIOG=
nbomen4tEH2yTkxvfBlLhx2aejCK-adTsT48J5_vu_UHdkjY_m9pxXuJu9sLzyOnYnbMHXNqDz6=
uqkoGCVzlGUQFZEgtnjha5fI3s5rg">Unsubscribe from all Typeform respondent not=
ifications</a>
