# $NetBSD: Makefile,v 1.14 2017/11/30 16:45:42 adam Exp $

DISTNAME=	kactivities-stats-${KF5VER}
PKGREVISION=	11
CATEGORIES=	x11

HOMEPAGE=	https://community.kde.org/Frameworks
COMMENT=	Core components for the KDE's Activities
LICENSE=	gnu-lgpl-v2 AND gnu-lgpl-v2.1 AND gnu-lgpl-v3

.include "../../meta-pkgs/kf5/Makefile.common"

PKGCONFIG_OVERRIDE+=	src/libKActivitiesStats.pc.cmake

.include "../../x11/kactivities5/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
