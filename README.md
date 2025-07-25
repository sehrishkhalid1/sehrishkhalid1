import React from 'react';
import { View, Text, Image, TouchableOpacity, Linking, ScrollView, StyleSheet } from 'react-native';

const socials = [
  {
    name: 'Facebook',
    url: 'https://facebook.com/muneer.ansari.1422?mibextid=ZbWKwL',
    logo: 'https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white',
  },
  {
    name: 'Instagram',
    url: 'https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white',
    logoLink: 'https://instagram.com/Muneerkhalid_',
  },
  {
    name: 'LinkedIn',
    url: 'https://linkedin.com/in/muneer-khalid-489079215',
    logo: 'https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white',
  },
];

const techStack = [
  {
    logo: 'https://img.shields.io/badge/react-%2320232a.svg?style=flat&logo=react&logoColor=%2361DAFB',
  },
  {
    logo: 'https://img.shields.io/badge/javascript-%23323330.svg?style=flat&logo=javascript&logoColor=%23F7DF1E',
  },
  {
    logo: 'https://img.shields.io/badge/html5-%23E34F26.svg?style=flat&logo=html5&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/css3-%231572B6.svg?style=flat&logo=css3&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54',
  },
  {
    logo: 'https://img.shields.io/badge/typescript-%23007ACC.svg?style=flat&logo=typescript&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/netlify-%23000000.svg?style=flat&logo=netlify&logoColor=#00C7B7',
  },
  {
    logo: 'https://img.shields.io/badge/vercel-%23000000.svg?style=flat&logo=vercel&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/bootstrap-%238511FA.svg?style=flat&logo=bootstrap&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/express.js-%23404d59.svg?style=flat&logo=express&logoColor=%2361DAFB',
  },
  {
    logo: 'https://img.shields.io/badge/jquery-%230769AD.svg?style=flat&logo=jquery&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/MUI-%230081CB.svg?style=flat&logo=mui&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/node.js-6DA55F?style=flat&logo=node.js&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/NODEMON-%23323330.svg?style=flat&logo=nodemon&logoColor=%BBDEAD',
  },
  {
    logo: 'https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=flat&logo=mongodb&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/mysql-%2300000f.svg?style=flat&logo=mysql&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/figma-%23F24E1E.svg?style=flat&logo=figma&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/Canva-%2300C4CC.svg?style=flat&logo=Canva&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=flat&logo=kubernetes&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/ESLint-4B3263?style=flat&logo=eslint&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/-jest-%23C21325?style=flat&logo=jest&logoColor=white',
  },
  {
    logo: 'https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white',
  },
];

const BadgeSection = () => {
  return (
    <ScrollView style={styles.container}>
      <Text style={styles.sectionTitle}>🌐 Socials</Text>
      <View style={styles.badgeRow}>
        {socials.map((item, idx) => (
          <TouchableOpacity key={idx} onPress={() => Linking.openURL(item.url)}>
            <Image source={{ uri: item.logo }} style={styles.badge} />
          </TouchableOpacity>
        ))}
      </View>

      <Text style={styles.sectionTitle}>💻 Tech Stack</Text>
      <View style={styles.badgeRow}>
        {techStack.map((item, idx) => (
          <Image key={idx} source={{ uri: item.logo }} style={styles.badge} />
        ))}
      </View>
    </ScrollView>
  );
};

const styles = StyleSheet.create({
  container: {
    padding: 16,
  },
  sectionTitle: {
    fontSize: 18,
    fontWeight: 'bold',
    marginVertical: 12,
  },
  badgeRow: {
    flexDirection: 'row',
    flexWrap: 'wrap',
    gap: 10,
  },
  badge: {
    height: 30,
    width: 'auto',
    resizeMode: 'contain',
    margin: 5,
  },
});

export default BadgeSection;
