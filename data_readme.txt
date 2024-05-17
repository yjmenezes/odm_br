# steps to use odm_br dataset
cd /tmp
git clone https://github.com/yjmenezes/odm_br.git
cd /tmp/odm_br
tar xjvf odm_gcp_br_2017-04-24.tar.bz2 -C ./
mkdir -p images
tar xjvf ./images_a.tar.bz2 -C ./images/
tar xjvf ./images_b.tar.bz2 -C ./images/
cp gcp_list.txt ./images/
# to run: cd to OpenDroneMap directory
# ./run.sh  /tmp/   odm_br
