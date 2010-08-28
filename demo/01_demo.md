!SLIDE 

# Installing / Configuring SPlat

    @@@ruby
    $ gem install josh-splat

    # For Rails apps
    $ ./script/generate splat 

    # Important configuration files
    $ config/splat.yml
    $ config/vendors.yml

!SLIDE 

# Demo1 - Send a simple SMS

!SLIDE 

# Demo1 - Send a simple SMS

    @@@ruby
    require 'lib/splat'
        
    number = '+91 9960054954'
    gw1 = Splat::Base.new(:clickatell)

    msg = "Fall SPlat on your face!"
    p gw1.send_sms(msg, number)

!SLIDE center 

# Demo2 - Multiple gateways together

!SLIDE 

# Multiple gateways together

    @@@ruby
    numbers=['+1 6096138032', '+91 9881395656']

    clickatell = Splat::Base.new(:clickatell)
    bulksms = Splat::Base.new(:bulksmspune)

    msg = "T: Fall SPlat on your face!"
    numbers.each do |number|
      if number =~ /^\+1\ /
        clickatell.send_sms(msg, number)
      elsif number =~ /^\+91\ /
        bulksms.send_sms(msg, number) 
      end
    end

!SLIDE

# Demo3 - Custom bulk messages 

!SLIDE

# Custom bulk messages 

    @@@ruby
    gw = Splat::Base.new(:clickatell)

    custom_msg = "Hi $1, hold on to your $2."
    options = {
     '+91 9960054954' => ['Jiren', 'shorts'],
     '+91 9881395656' => ['Gautam' , 'stocks'],
     '+91 9880397111' => ['Jane' , 'coffee']
    }

    gw.send_bulk_sms_with_insertion(custom_msg,
                                options)
