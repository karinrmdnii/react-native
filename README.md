# react-native
project uts abp gek hanuy karin
import React from "react";
import { View, Text, StyleSheet, TouchableOpacity, ScrollView } from "react-native";

export default function HomeScreen({ navigation }) {
  return (
    <ScrollView style={styles.container}>
      <Text style={styles.title}>Mental Health</Text>

      {/* Quote of the Day */}
      <Text style={styles.sectionTitle}>Quote of the Day</Text>
      <View style={styles.card}>
        <Text style={styles.quote}>
          "The greatest wealth is mental health." – Virgil
        </Text>
      </View>

      {/* Journal Button */}
      <Text style={styles.sectionTitle}>Your Journal</Text>
      <TouchableOpacity
        style={styles.journalButton}
        onPress={() => navigation.navigate("WriteJournal")}
      >
        <Text style={styles.journalButtonText}>✏ Write a Journal</Text>
      </TouchableOpacity>

      {/* Recent Journals */}
      <Text style={styles.sectionTitle}>Daily Journaling</Text>

      <View style={styles.card}>
        <Text style={styles.date}>June 05, 2024</Text>
        <Text style={styles.entryTitle}>Today I felt quite anxious.</Text>
        <Text style={styles.entryText}>
          I’m struggling to manage stress at work.
        </Text>
      </View>

      <View style={styles.card}>
        <Text style={styles.date}>June 04, 2024</Text>
        <Text style={styles.entryTitle}>I'm grateful for the support.</Text>
        <Text style={styles.entryText}>
          I feel better after talking to my friend.
        </Text>
      </View>

    </ScrollView>
  );
}

const styles = StyleSheet.create({
  container: {
    backgroundColor: "#F1E4D3",
    padding: 20,
  },
  title: {
    fontSize: 26,
    fontWeight: "bold",
    textAlign: "center",
    marginBottom: 20,
  },
  sectionTitle: {
    fontSize: 18,
    fontWeight: "bold",
    marginTop: 15,
    marginBottom: 8,
  },
  card: {
    backgroundColor: "#F7ECD8",
    padding: 15,
    borderRadius: 15,
    marginBottom: 15,
  },
  quote: {
    fontSize: 16,
    fontStyle: "italic",
  },
  journalButton: {
    backgroundColor: "#F7ECD8",
    padding: 15,
    borderRadius: 15,
    alignItems: "center",
    marginBottom: 20,
  },
  journalButtonText: {
    fontSize: 16,
    fontWeight: "bold",
  },
  date: {
    fontSize: 12,
    marginBottom: 4,
    color: "#4A4A4A",
  },
  entryTitle: {
    fontSize: 16,
    fontWeight: "bold",
  },
  entryText: {
    fontSize: 14,
    color: "#444",
    marginTop: 4,
  },
});
