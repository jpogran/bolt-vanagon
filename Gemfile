source 'https://rubygems.org'

def location_for(place)
  if place =~ /^(git[:@][^#]*)#(.*)/
    [{ :git => $1, :branch => $2, :require => false }]
  elsif place =~ /^file:\/\/(.*)/
    ['>= 0', { :path => File.expand_path($1), :require => false }]
  elsif place =~ /(\d+\.\d+\.\d+)/
    [ place, { :require => false }]
  end
end

gem "beaker-hostgenerator", *location_for(ENV['BEAKER_HOSTGENERATOR_VERSION'] || "~> 0.7")
gem "beaker-abs", *location_for(ENV['BEAKER_ABS_VERSION'] || "~> 0.1")
gem 'vanagon', *location_for(ENV['VANAGON_LOCATION'] || '~> 0.19')
gem 'packaging', *location_for(ENV['PACKAGING_LOCATION'] || '~> 0.99.8')
gem 'json'
gem 'rake'
