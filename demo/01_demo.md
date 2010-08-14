!SLIDE commandline incremental

# Example - Send customized SMS in bulk

    $ gw1 = Splat::Base.new('clickatell')
    <% Spat::Base#>
    $ gw1.send_bulk_sms("Hi %s asdf",
              :options => { 'a' => 'b',
                             1 => 2 
              })
    irb> Sent

!SLIDE 

# Installing SPlat

    $ gem install splat

!SLIDE

# Initializing the SMS gateways

!SLIDE

# Configuring SPlat

!SLIDE bullets

# Mobile number formats

* +1 501-234-8473
* 001 5012348473
* +5012348473
* 5012348473
* All vendors have their own formats.

!SLIDE

# Splat default number format

    @@@ruby
    /^\+\d{1,4}\ \d{8,12}$/  # +91 9812345867


!SLIDE bullets incremental

# Splat callback

* Application can register a callback.
* :before_send 
* Manipulate the number to splat format.

!SLIDE bullets 

# Demo1 - simple send SMS

* Send SMS via vMobo
* Show the vMobo report

!SLIDE bullets 

# Demo2 - switch gateways

* Change vMobo to bulksms
* Show the bulksms report

!SLIDE bullets 

# Demo3 - both together

* Show reports in both

!SLIDE bullets 

# Demo4 - custom bulk SMS

* Customized SMS via vMobo and bulksms
