!SLIDE bullets 

# What is <span class="splat">SPlat</span>?

* A library for Ruby SMS APIs.
* Automatically integrates with different vendors.
* Packaged in a Ruby gem.
* http://rubygems.org/gems/josh-splat

!SLIDE bullets

# What <span class="splat">SPlat</span> is NOT?

* SPlat is not a SMS gateway or service provider
* You still have to purchase SMS gateway subscription
* <span class='highlight'>SPlat makes choices simple </span>
* <span class='highlight'>You can afford to make mistakes!</span>

!SLIDE bullets 

# <span class='splat'>SPlat</span> Features

* Change SMS gateway without changing code.
* <span class='highlight'>Multiple</span> SMS gateways simultaneously!
* Send customized bulk messages for any vendor.
* Test via bogus SMS gateway.

!SLIDE bullets

# <span class='splat'>SPlat</span> Features

* Schedule sending SMS.
* Manage tagged lists for sending bulk SMS
* Standardized status and statistical reports
* Trend Analysis

!SLIDE center

# Challenges we faced 

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


!SLIDE bullets 

# Splat callback

* Application can register a callback.
* :before_send 
* Manipulate the number to splat format.

