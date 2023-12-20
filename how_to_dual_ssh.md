Para aquellos casos donde tengamos por un lado una cuenta personal de GitHub (o similar) y una cuenta de empresa, podemos tener 

Lo primero que debemos hacer es crear para la nueva maquina dos claves SSH. Una para profesional y otra para personal:
`ssh-keygen -t rsa -C "fernando.rodriguez@nielseniq.com"`

[El siguiente paso es crear el archivo config para permitir multiples hosts](https://gist.github.com/jexchan/2351996):

`/home/azureuser/.ssh/config`

```
# Personal account
Host github.com-ferjorosa
	HostName github.com
	User git
	IdentityFile ~/.ssh/id_rsa_ferjorosa

# Professional account
Host github.com-niq
	HostName github.com
	User git
	IdentityFile ~/.ssh/id_rsa_niq
```

Finalmente, podemos clonar desde diferentes hosts:

git clone git@github.com-niq:niq-enterprise/ainn-omnisales-latam-data-prep.git
git clone git@github.com-ferjorosa:ferjorosa/learn-ebit.git
