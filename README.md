#Socketstream passport rpc middleware
##Usage example

#### middleware/passport.coffee  
    passport    = require 'passport'
    ssPassport  = require 'ss-passport-request'
    
    exports.initialize = (options = {}) ->
      return passport.initialize()       
    
    exports.session = (options = {}) ->
      return passport.session()  
    
    exports.req = (options = {})->
      return ssPassport

#### rpc/...            
    req.use "session"
    req.use "passport.initialize"
    req.use "passport.session"
    req.use "passport.req"