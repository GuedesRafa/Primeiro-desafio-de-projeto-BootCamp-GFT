# Passo a passo para Criar sua chave SSH:closed_lock_with_key: :key:

### O processo de criação e validação de uma chave SSH é feito em 3 etapas:

- **1** - Criação da chave no GtBash;
- **2** - Passar a chave pública para o Github;
- **3** - Válidar a chave pessoal com o "Agent" do Git.



**Passo 1**: 

	- Abrir o Git.
	- Digite: SSH-keygen -t ed25519 -C (Seu email do Github);
	- Crie uma senha;
	- Digite: (O caminho até a pasta **.SSH** )
	- Estando dentro da pasta **.SSH**: Digite o comando **ls** para listar os arquivos dentro da pasta e verifique se a chave está lá.
	- Digite: cat id_ed25519.pub (Irá visualizar o conteúdo da chave publica).

**Passo 2:**

- Abra o Github;
- Vá em **Chave SSH** e em **Nova chave**;
- Copie o conteúdo da chave publica (HASH) e cole no campo disponível.

**Passo 3**

- Volte ao GitBash e crie o "agent". Digite: eval $ (SSH - agent -s)
- Digite: SSH-add id_ed25519
- confirme a senha.

