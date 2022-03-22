read -p "ESCOLHA UM FORMATO DO DOCKER, QUE É SUPORTADO POR SUA VPS (docker ou docker.io): " docker && apt update && apt install $docker -y && read -p "EM QUAL PORTA, VOCÊ DESEJAR INSTALAR O SERVIDOR CHISEL? " porta && read -p "DEFINA UM NOME DE USUÁRIO PARA O CHISEL:  " username && read -p "DEFINA UMA SENHA PARA O CHISEL: " password && docker run --name chisel -p $porta:$porta -d --restart always jpillora/chisel server -p $porta --socks5 --key supersecret --auth "$username:$password" 

apt install curl -y
curl ipv4.icanhazip.com

read -p "ESCOLHA UM FORMATO DO DOCKER, QUE É SUPORTADO POR SUA VPS (docker ou docker.io): " docker && $docker start chisel

read -p "ESCOLHA UM FORMATO DO DOCKER, QUE É SUPORTADO POR SUA VPS (docker ou docker.io): " docker && $docker stop chisel

read -p "ESCOLHA UM FORMATO DO DOCKER, QUE É SUPORTADO POR SUA VPS (docker ou docker.io): " docker && $docker stop chisel && $docker rm chisel
