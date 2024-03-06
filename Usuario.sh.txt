echo "Criando usuários do sistema...."

for i in {10..13}
do
    useradd "guest$i" -c "Usuário convidado" -s /bin/bash -m -p $(openssl passwd -crypt Senha123)
    passwd "guest$i" -e
done

echo "Finalizado!!"
