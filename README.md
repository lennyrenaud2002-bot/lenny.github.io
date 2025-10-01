[index (1).html](https://github.com/user-attachments/files/22645922/index.1.html)<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selectra - Checklist Commerciale</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="app-container">
        <div class="sidebar">
            <!-- Header avec logo et timer -->
            <div class="sidebar-header">
                <div class="logo">
                    <span class="logo-icon">⚡</span>
                    <span class="logo-text">SELECTRA</span>
                </div>
                <div class="call-timer">
                    <span class="timer-icon">⏱️</span>
                    <span id="call-time">00:00</span>
                </div>
            </div>

            <!-- Contenu scrollable -->
            <div class="sidebar-content">
                <!-- Section Informations Client -->
                <section class="checklist-section" data-section="client">
                    <div class="section-header">
                        <h3>📝 Informations Client</h3>
                        <span class="counter" id="client-counter">0/8</span>
                    </div>
                    <div class="section-content">
                        <div class="form-group">
                            <label for="nom">Nom</label>
                            <input type="text" id="nom" name="nom" placeholder="Nom du client" required>
                        </div>
                        <div class="form-group">
                            <label for="prenom">Prénom</label>
                            <input type="text" id="prenom" name="prenom" placeholder="Prénom du client" required>
                        </div>
                        <div class="form-group">
                            <label for="adresse">Adresse</label>
                            <textarea id="adresse" name="adresse" placeholder="Adresse complète, CP, Ville" required></textarea>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" name="email" placeholder="email@exemple.fr" required>
                        </div>
                        <div class="form-group">
                            <label for="telephone">Téléphone</label>
                            <input type="tel" id="telephone" name="telephone" placeholder="06 XX XX XX XX" required>
                        </div>
                        <div class="form-group">
                            <label for="pdl">PDL (14 chiffres)</label>
                            <input type="text" id="pdl" name="pdl" placeholder="14 chiffres PDL">
                        </div>
                        <div class="form-group">
                            <label for="pce">PCE (14 chiffres)</label>
                            <input type="text" id="pce" name="pce" placeholder="14 chiffres PCE">
                        </div>
                        <div class="form-group">
                            <label for="iban">IBAN</label>
                            <input type="text" id="iban" name="iban" placeholder="FR76..." class="secure-field">
                        </div>
                    </div>
                </section>

                <!-- Section Accords Explicites -->
                <section class="checklist-section" data-section="accords">
                    <div class="section-header">
                        <h3>✅ Accords Explicites</h3>
                        <span class="counter" id="accords-counter">0/6</span>
                    </div>
                    <div class="section-content">
                        <label class="checkbox-item obligatoire">
                            <input type="checkbox" name="rgpd_donnees" required>
                            <span class="checkmark"></span>
                            <span class="label-text">RGPD données</span>
                            <span class="badge obligatoire">OBLIGATOIRE</span>
                        </label>
                        <label class="checkbox-item obligatoire">
                            <input type="checkbox" name="acces_reseau" required>
                            <span class="checkmark"></span>
                            <span class="label-text">Accès réseau Enedis/GRDF</span>
                            <span class="badge obligatoire">OBLIGATOIRE</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="voltalis_rdv">
                            <span class="checkmark"></span>
                            <span class="label-text">Voltalis RDV planifié</span>
                        </label>
                        <label class="checkbox-item payant">
                            <input type="checkbox" name="axa_assistance" data-payant="true">
                            <span class="checkmark"></span>
                            <span class="label-text">AXA Assistance 6,99€</span>
                            <span class="badge payant">PAYANT</span>
                        </label>
                        <label class="checkbox-item payant">
                            <input type="checkbox" name="compensation_carbone" data-payant="true">
                            <span class="checkmark"></span>
                            <span class="label-text">Compensation Carbone</span>
                            <span class="badge payant">PAYANT</span>
                        </label>
                        <label class="checkbox-item payant">
                            <input type="checkbox" name="conseiller_perso" data-payant="true">
                            <span class="checkmark"></span>
                            <span class="label-text">Mon Conseiller Perso</span>
                            <span class="badge payant">PAYANT</span>
                        </label>
                    </div>
                </section>

                <!-- Section Mentions Légales -->
                <section class="checklist-section" data-section="mentions">
                    <div class="section-header">
                        <h3>⚖️ Mentions Légales</h3>
                        <span class="counter" id="mentions-counter">0/5</span>
                    </div>
                    <div class="section-content">
                        <label class="checkbox-item timer-item">
                            <input type="checkbox" name="axa_exclusions">
                            <span class="checkmark"></span>
                            <span class="label-text">AXA 4 exclusions</span>
                            <span class="timer-badge">30s min</span>
                        </label>
                        <label class="checkbox-item timer-item">
                            <input type="checkbox" name="axa_rgpd">
                            <span class="checkmark"></span>
                            <span class="label-text">AXA RGPD + durée</span>
                            <span class="timer-badge">20s min</span>
                        </label>
                        <label class="checkbox-item timer-item">
                            <input type="checkbox" name="carbone_processus">
                            <span class="checkmark"></span>
                            <span class="label-text">Carbone processus</span>
                            <span class="timer-badge">15s min</span>
                        </label>
                        <label class="checkbox-item obligatoire">
                            <input type="checkbox" name="frais_mes" required>
                            <span class="checkmark"></span>
                            <span class="label-text">Frais MES communiqués</span>
                            <span class="badge obligatoire">OBLIGATOIRE</span>
                        </label>
                        <label class="checkbox-item obligatoire">
                            <input type="checkbox" name="delai_retractation" required>
                            <span class="checkmark"></span>
                            <span class="label-text">Délai rétractation 14j</span>
                            <span class="badge obligatoire">OBLIGATOIRE</span>
                        </label>
                    </div>
                </section>

                <!-- Section Signatures SMS -->
                <section class="checklist-section" data-section="sms">
                    <div class="section-header">
                        <h3>📱 Signatures SMS</h3>
                        <span class="counter" id="sms-counter">0/3</span>
                    </div>
                    <div class="section-content">
                        <label class="checkbox-item">
                            <input type="checkbox" name="code_axa">
                            <span class="checkmark"></span>
                            <span class="label-text">Code AXA reçu/validé</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="code_carbone">
                            <span class="checkmark"></span>
                            <span class="label-text">Code Carbone reçu/validé</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="code_mcp">
                            <span class="checkmark"></span>
                            <span class="label-text">Code MCP reçu/validé</span>
                        </label>
                    </div>
                </section>

                <!-- Section Étapes Commerciales -->
                <section class="checklist-section" data-section="etapes">
                    <div class="section-header">
                        <h3>🎯 Étapes Commerciales</h3>
                        <span class="counter" id="etapes-counter">0/7</span>
                    </div>
                    <div class="section-content">
                        <label class="checkbox-item">
                            <input type="checkbox" name="client_qualifie">
                            <span class="checkmark"></span>
                            <span class="label-text">Client qualifié correctement</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="besoins_analyses">
                            <span class="checkmark"></span>
                            <span class="label-text">Besoins analysés</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="offre_presentee">
                            <span class="checkmark"></span>
                            <span class="label-text">Offre présentée clairement</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="objections_traitees">
                            <span class="checkmark"></span>
                            <span class="label-text">Objections traitées</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="addons_proposes">
                            <span class="checkmark"></span>
                            <span class="label-text">Add-ons proposés (min 2 payants)</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="signatures_obtenues">
                            <span class="checkmark"></span>
                            <span class="label-text">Signatures obtenues</span>
                        </label>
                        <label class="checkbox-item">
                            <input type="checkbox" name="recap_final">
                            <span class="checkmark"></span>
                            <span class="label-text">Récap final effectué</span>
                        </label>
                    </div>
                </section>

                <!-- Section Notes d'Appel -->
                <section class="checklist-section" data-section="notes">
                    <div class="section-header">
                        <h3>📋 Notes d'Appel</h3>
                    </div>
                    <div class="section-content">
                        <textarea id="notes" name="notes" placeholder="Observations importantes, objections client, remarques particulières..."></textarea>
                        <div class="notes-actions">
                            <button type="button" class="btn-secondary" id="clear-notes">Effacer</button>
                            <button type="button" class="btn-primary" id="save-notes">Sauvegarder</button>
                        </div>
                    </div>
                </section>

                <!-- Section Résumé Final -->
                <section class="checklist-section resume" data-section="resume">
                    <div class="section-header">
                        <h3>📊 Résumé Final</h3>
                    </div>
                    <div class="section-content">
                        <div class="resume-grid">
                            <div class="resume-item">
                                <span class="resume-label">✓ Informations :</span>
                                <span class="resume-value" id="resume-client">0/8</span>
                            </div>
                            <div class="resume-item">
                                <span class="resume-label">✓ Accords :</span>
                                <span class="resume-value" id="resume-accords">0/6</span>
                            </div>
                            <div class="resume-item">
                                <span class="resume-label">✓ Services payants :</span>
                                <span class="resume-value" id="resume-payants">0/3 (min 2)</span>
                            </div>
                            <div class="resume-item">
                                <span class="resume-label">✓ Mentions :</span>
                                <span class="resume-value" id="resume-mentions">0/5</span>
                            </div>
                            <div class="resume-item">
                                <span class="resume-label">✓ Étapes :</span>
                                <span class="resume-value" id="resume-etapes">0/7</span>
                            </div>
                        </div>
                        <div class="progress-section">
                            <div class="progress-bar">
                                <div class="progress-fill" id="progress-fill" style="width: 0%"></div>
                            </div>
                            <div class="progress-text">
                                <span>Progression : </span>
                                <span id="progress-percentage">0%</span>
                            </div>
                        </div>
                        <div class="validation-alerts" id="validation-alerts"></div>
                    </div>
                </section>
            </div>

            <!-- Footer fixe avec actions -->
            <div class="sidebar-footer">
                <button type="button" class="btn-export" id="export-txt">
                    <span class="btn-icon">📄</span>
                    <span class="btn-text">Export .txt</span>
                </button>
                <button type="button" class="btn-reset" id="reset-all">
                    <span class="btn-icon">🔄</span>
                    <span class="btn-text">Reset</span>
                </button>
            </div>
        </div>
    </div>

    <!-- Modal de confirmation pour reset -->
    <div class="modal hidden" id="reset-modal">
        <div class="modal-content">
            <h3>⚠️ Confirmation Reset</h3>
            <p>Êtes-vous sûr de vouloir effacer toutes les données ?</p>
            <div class="modal-actions">
                <button type="button" class="btn-secondary" id="cancel-reset">Annuler</button>
                <button type="button" class="btn-danger" id="confirm-reset">Confirmer</button>
            </div>
        </div>
    </div>

    <script src="app.js"></script>
</body>
</html>
