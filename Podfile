# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'OpenCV' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!
  
  # Pods for OpenCV
  
  pod 'OpencvQueen', :path => './'
  
  pod 'Masonry'
  pod 'KJCategories' # 开发加速库
  pod 'KJCategories/C7/UINavigation'
  pod 'KJCategories/C7/UIViewController'
  
end

## Ignore CocoaPods warnings
inhibit_all_warnings!
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['COMPILER_INDEX_STORE_ENABLE'] = "NO"
      if config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'].to_f < 10.0
        config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '10.0'
      end
    end
  end
end
