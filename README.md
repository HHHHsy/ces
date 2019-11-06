#
阿里云maven配置

buildscript {
    repositories {

        // 添加阿里云 maven 地址
        maven { url 'http://maven.aliyun.com/nexus/content/groups/public/' }
        maven { url 'http://maven.aliyun.com/nexus/content/repositories/jcenter' }

        google()
        jcenter()

    }
    dependencies {
        classpath 'com.android.tools.build:gradle:3.5.2'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

allprojects {
    repositories {

        // 添加阿里云 maven 地址
        maven { url 'http://maven.aliyun.com/nexus/content/groups/public/' }
        maven { url 'http://maven.aliyun.com/nexus/content/repositories/jcenter' }

        google()
        jcenter()
        maven { url "https://jitpack.io" }

    }
}

task clean(type: Delete) {
    delete rootProject.buildDir
}
