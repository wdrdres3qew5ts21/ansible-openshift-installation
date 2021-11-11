## Ansible Openshift Installer
ใช้คำสั่ง `./setup_openshift.sh -e openshift_token=$TOKEN` ในการติดตั้งโปรเจคให้เรียบร้อย
แล้วเราจะได้ Ansible Tower ขึ้นมาให้เราทำการกรอก Credentials ที่ใช้งานให้ถูกต้อง

1. ansiblejob ต้องอยุ่ namespace เดียวกับ subscription ที่ deploy
2. ansiblejob ต้องเข้าถึง secret ไปหา Tower GUI ได้
3. ansible Tower ต้องตั้งค่าอนุญาตรับ prompt override value
4. Domain ใช้ได้ทั้ง HTTP และ HTTPS ดังนั้นเรียก Ansible Tower ใน Cluster ตัวเองก็ได้

Collection ของ Policy 
https://github.com/open-cluster-management/policy-collection/tree/main/community

Run Policy on violation
https://cloud.redhat.com/blog/initiating-ansible-automation-on-policy-violations