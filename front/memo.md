 # ssh -i "seongmin-webpc.pem" ubuntu@ec2-18-117-151-106.us-east-2.compute.amazonaws.com

 # nginx

 sudo apt-get install nginx
 도중에 [y/n] 나오면 y 눌러주세요

 nginx.conf : 설정파일
sites-availabel : (폴더)
sites-enabled : (폴더)

sites-availabel > 설정파일 만들고
sites-enabled > 바로가기 셋팅하게

nginx 실행

vi 많이 쓸거임

cp 명령어
copy
mv
move

sudo vi myapp.conf


server{
    listen 80; // 포트실행번호
    location / { // uri 값
        root /home/ubuntu/www //내가 실행시킬 파일 경로
        index index.html index.htm; //내가 실행시킬 파일명
        try_files $uri /index.html; //http://localhost:3000/about

    }
}

ln -s [기존디렉토리] [바로가기만들디렉토리]

sudo nginx -t

/etc/nginx

cd sites-enabled

sudo rm myapp.conf

sudo ln -s /etc/nginx/sites-available/myapp.conf /etc/nginx/sites-enabled/myapp.conf

/etc/nginx
sudo nginx -t

sudo systemctl start nginx
sudo systemctl stop nginx

















