Vagrant.configure("2") do |config|
  config.vm.box = "centos7"
  config.vm.network "private_network", ip: "192.168.33.12"

  # ゲストOSと共有するディレクトリの設定
  # 共有ディレクトリはゲストOS側でパーミッションの変更が出来ないため、mount_optionsで指定
  config.vm.synced_folder "./src/", "/var/www/html/", :owner=> 'vagrant', :group=>'wheel', :mount_options => ['dmode=775', 'fmode=775']

  # provisionにansibleを使う設定
  config.vm.provision "ansible" do |ansible|
    ansible.limit = 'all'
    ansible.inventory_path = "hosts"
    ansible.playbook = "provisioning/playbook.yml"
  end
end

