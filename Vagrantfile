# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
# すべてのvagrant設定は以下に記述する。Vagrant.configureの引数"2"は
# 設定バージョンです（上位互換性のために古い設定方法をサポートしています）。
# よく知らない限り変更しないでください。
Vagrant.configure(2) do |config|

  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.
  # もっとも一般的な設定オプションは、ここから下に記述されています。
  # すべての設定を確認する場合はオンラインドキュメントを以下のリンクから
  # 参照してください。
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  # すべてのVagrant開発環境はboxを必要とする。以下のリンクからboxを探せます。
  # https://atlas.hashicorp.com/search.
  config.vm.box = "centos6-chef"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # boxのアップデートの自動チェックを行わないようにする。
  # もし行わない場合、'古いvagrant box'を実行した時にだけboxのアップデートがチェックされる。
  # これは推奨しない。
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # ホストPC上のポートから同マシン上の特定のポートにアクセスするようにポートフォワーディングのマッピングを作成する。
  # 例えば以下の場合、"localhost:8080"へのアクセスは、ゲストマシンにポート80でフォワーディングされる。
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # 特定のIPを使ってマシンにhost-only接続を行えるようにするプライベートネットワークを作成する
  config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # ブリッジネットワークと同調するパブリックネットワークを作成する。
  # ブリッジネットワークは、マシンを同じネットワーク上に存在する別の物理デバイスとして扱う。
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # ゲストOSに共有フォルダを追加する。第一引数はホスト上の共有元フォルダパス。
  # 第２引数はゲスト上の共有先フォルダパス。
  # 第３引数はオプショナルで、任意のオプションを連ねた配列です。
  config.vm.synced_folder ".", "/vagrant", mount_options:['dmode=777','fmode=777']

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  # プロバイダ特有の設定なので、様々なプロバイダをVagrant向けに調整できる。
  # これらはプロバイダ特有のオプションを陳列する。
  # VirtualBoxの例を示す：
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   # 仮想マシンをブーとした時、VirtualBoxのGUIを表示する。
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   # VMに割り当てるメモリ量をカスタマイズする
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.
  # 利用可能なオプションについてはさらに詳しい情報が必要な場合は
  # 利用している各プロバイダのドキュメントをみてください。

  # Define a Vagrant Push strategy for pushing to Atlas. Other push strategies
  # such as FTP and Heroku are also available. See the documentation at
  # https://docs.vagrantup.com/v2/push/atlas.html for more information.
  # AtolasをプッシュするためのVagrant Push strategyを定義する。
  # FTPやHerokuのような他のPush strategyでも可です。
  # より多くの情報はhttps://docs.vagrantup.com/v2/push/atlas.html参照
  # config.push.define "atlas" do |push|
  #   push.app = "YOUR_ATLAS_USERNAME/YOUR_APPLICATION_NAME"
  # end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # shell scriptによるプロビジョニングを可能にする.
  # PuppetやChef、Ansible、salt、Dockerのような追加プロビジョナーでも可能です。
  # より詳細な情報はドキュメントを読んでください。
  # config.vm.provision "shell", inline: <<-SHELL
  #   sudo apt-get update
  #   sudo apt-get install -y apache2
  # SHELL
end
