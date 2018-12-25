docker run -d \
     -e PASSWORDENV=my_secret \
     -e IPENV=my_IP \
     -e ROOTDNENV=my_rootdn \
     -e HOSTENV=myhostname \
     -e URLCAEXTRACTENV=urltoextractca \
     -e CAFILEENV=myfilecacert
     -p 389:389 \
     -p 636:636 \
     --privileged \
     santinoncs/openldap-to-ad-proxy


看了一下配置文件，感觉有些配置好麻烦呀，到时候改一下
其实还有一个文件夹certs，里面放了私钥证书，公钥证书
使用url的方式来获取，所以上面的参数名解释一下
URLCAEXTRACTENV -> CA证书URL地址(pem)
CAFILEENV -> 在certs中的证书文件

