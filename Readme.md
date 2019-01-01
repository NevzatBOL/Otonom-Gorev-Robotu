# Otonom Görev Robotu

nevbot Dosyası indirildikten sonra dosya içerisinde 'catkin_make' yapılarak dosyanın ros bağlantıları yapılır.

Robotu Gazebo Simülasyon ortamında çalıştırmak için;

    roslaunch nevbot_gazebo model.launch 

Robotu Rviz Simülasyon ortamında çalıştırmak için;

    roslaunch nevbot_description view_model.launch 

Robot ile harita çıkarma için öncelikle robot gazebo ortamında çalıştırılır.

    roslaunch nevbot_gazebo model.launch 

Hektor Mapping ile haritalama yapmak için;

    roslaunch nevbot_navigation hectormapping.launch 
    
Gmapping ile haritalama yapmak için;    
    
    roslaunch nevbot_navigation gmapping.launch 

Karto ile haritalama yapmak için;

    roslaunch nevbot_navigation karto.launch 

Haritalama paketlerinden biri çalıştırıldıktan sonra rviz paketi çalıştırılır.

    roslaunch nevbot_description view_mapping.launch 
    
Oluşturulan haritayı kaydetmek için;

    rosrun map_server map_saver -f test.yaml

Oluşturulan harita üzerinde navigation yapmak için;

    roslaunch nevbot_gazebo model.launch 
    
    Oluşturulan haritayı yüklemek için;
    
    roslaunch nevbot_navigation amcl.launch     
    
    roslaunch nevbot_description view_mapping.launch 

Robotun Joystick ile kontrolü için;

    roslaunch nevbot_control joy.launch 

Robotun Klavye üzerinden kontrolü için;

    roslaunch nevbot_control teleop.launch 

