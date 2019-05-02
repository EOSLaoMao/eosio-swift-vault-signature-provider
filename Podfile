using_local_pods = false

unless using_local_pods
  source 'https://github.com/EOSIO/eosio-swift-pod-specs.git'
  source 'https://github.com/CocoaPods/Specs.git'
end

platform :ios, '11.3'

if using_local_pods
  # Pull pods from sibling directories if using local pods
  target 'EosioSwiftVaultSignatureProvider' do
    use_frameworks!

    pod 'EosioSwift', :path => '../eosio-swift'
    pod 'EosioSwiftEcc', :path => '../eosio-swift-ecc'
    pod 'EosioSwiftVault', :path => '../eosio-swift-vault'
    pod 'SwiftLint'

    target 'EosioSwiftVaultSignatureProviderTests' do
      inherit! :search_paths
      pod 'EosioSwift', :path => '../eosio-swift'
      pod 'EosioSwiftEcc', :path => '../eosio-swift-ecc'
      pod 'EosioSwiftVault', :path => '../eosio-swift-vault'
    end
  end
else
  # Pull pods from sources above if not using local pods
  target 'EosioSwiftVaultSignatureProvider' do
    use_frameworks!

    pod 'EosioSwift', '~> 0.0.3'
    pod 'EosioSwiftEcc', '~> 0.0.3'
    pod 'EosioSwiftVault', '~> 0.0.3'
    pod 'SwiftLint'

    target 'EosioSwiftVaultSignatureProviderTests' do
      inherit! :search_paths
      pod 'EosioSwift', '~> 0.0.3'
      pod 'EosioSwiftEcc', '~> 0.0.3'
      pod 'EosioSwiftVault', '~> 0.0.3'
    end
  end
end